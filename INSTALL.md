<div title="header">

  

</div>

<div id="TextSection" dir="ltr">

<span class="sd-abs-pos" style="position: absolute; top: 0in; left: 0in; width: 343px">![](Virtual%20Network%20Orchestrator%20\(ViNO\)%20Installation%20Guide_html_ecc8317a0e8f7dff.png)
</span>

Virtual Network Orchestrator (ViNO) Installation Guide

Software Version 1.0.1

February 3, 2020

  
  

&copy;2020 CenturyLink. All Rights Reserved. The CenturyLink mark, pathways
logo and certain CenturyLink product names are the property of
CenturyLink. All other marks are the property of their respective
owners.
</div>

<div id="Table of Contents1" dir="ltr">

<div id="Table of Contents1_Head" dir="ltr">

## Contents

</div>

[Introduction](#Introduction)

[System Requirements](#System-Requirements)

[ViNO Installation Process](#ViNO-Installation-Process)

[Installing ViNO](#Installing-ViNO)

[Creating a Keycloak Realm for ViNO](#Creating-a-Keycloak-Realm-for-ViNO)

[ViNO Keycloak Roles and Groups](#ViNO-Keycloak-Roles-and-Groups)

[Populating the Keycloak Realm for ViNO](#Populating-the-Keycloak-Realm-for-ViNO)

[Adding Roles in Keycloak](#Adding-Roles-in-Keycloak)

[Adding a Group in Keycloak](#Adding-a-Group-in-Keycloak)

[Adding a User in Keycloak](#Adding-a-User-in-Keycloak)

[Adding a ViNO Client in Keycloak](#Adding-a-ViNO-Client-in-Keycloak)

[Initializing ViNO](#Initializing-ViNO)

[Logging in to ViNO](#Logging-in-to-ViNO)

</div>

List of Tables

<div id="Table of Figures" dir="ltr">

[Table 1. ViNO Keycloak Roles and Permissions](#Table_1)

[Table 2. Keycloak Task-to-Role Permissions](#Table_2)

</div>

  

## Introduction

This document describes how to install and initialize a ViNO instance
and how to create a realm in Keycloak.

ViNO uses the
<span style="text-decoration: none">[Keycloak](https://www.keycloak.org/)</span>
authentication server to provide local authentication and the ability to
incorporate federated authentication methods such as Kerberos or LDAP.
In addition, ViNO can use Single Sign On (SSO) Identity Providers (IdPs)
over SAML or OpenID Connect (OIDC).

In addition to this guide, ViNO documentation includes the *Virtual
Network Orchestrator (ViNO) User Guide*.

The VINO project was developed and tested on CentOS release 7.6.

## System Requirements

VINO is designed to be installed on a new minimal installation of
[CentOS
7.6](http://mirrors.oit.uci.edu/centos/7.6.1810/isos/x86_64/CentOS-7-x86_64-Minimal-1810.iso).
Ensure that your newly created CentOS machine is able to communicate on
the internet because it needs to download several components as part of
the VINO installation.

Before you download the VINO project, ensure that your workstation meets
or exceeds the following hardware requirements:

• A minimum of 4 CPUs

• A minimum of 20 GB of free disk space

• A minimum of 8 GB of RAM

## ViNO Installation Process

The following sections describe the complete process of installing and
initializing ViNO in addition to creating and populating a Keycloak
realm.

The order in which the process must be completed is as follows:

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Installing
    ViNO</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Creating
    a Keycloak Realm for ViNO</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Populating
    the Keycloak Realm for ViNO</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Initializing
    ViNO</span></span>

### Installing ViNO

To install an instance of ViNO instance:

1.  Download the ViNO installation file
    (vino-product-docker.1.0.1-4.tar.gz) from Github. For example:

        curl -LJO https://github.com/CenturyLink-ViNO/vino-product/releases/download/1.0.1/vino-product-docker.1.0.1-9.tar.gz

2.  Run the installation script: **sh ./binstall.sh**. The installation
    takes several minutes. When it installs successfully, the following
    messages are displayed:

        $ ViNO ---\> The ViNO docker images have been loaded. Please see the
        *Virtual Network Orchestrator (ViNO) Installation Guide* for detailed
        instructions on how to set up and run ViNO.
        
        $ ViNO ---\> log available in /var/log/vino.install/ViNO Docker
        Distribution\_product\_Install.1359.log.
        
        If the installation does not install properly, check the log file for
        error messages. Log files are located in /var/log/vino.install.

3.  Proceed to
    <span style="text-decoration: none"><span style="background: #c0c0c0">Creating
    a Keycloak Realm for ViNO</span></span>.

### Creating a Keycloak Realm for ViNO

After ViNO has been installed, you must create a Keycloak realm. ViNO
uses [Keycloak](https://www.keycloak.org/) for authorization.

To create a Keycloak realm:

1.  Use the command line to navigate to the directory: 
       
        /opt/vino/vino-docker

2.  From the directory, run the following command to start the four docker containers for ViNO.

        docker-compose -p vino up -d

3.  Open an internet browser and enter the IP address of your ViNO host
    in the URL bar followed by /auth (for example: 123.45.6.789/auth).
    This URL goes to the Keycloak homepage.

4.  Click **Administration Console**, which prompts you to log with the
    default username **admin** and default password **changethis**. We
    recommend changing the default password.

5.  From the **Master** drop-down, select **Add Realm**.

6.  Enter **vino** in the **Name** field, then click Create.

Proceed to the next sections for information on:

  - Keycloak roles and groups.

  - Adding roles, groups, users, and clients in Keycloak.

### ViNO Keycloak Roles and Groups

ViNO Keycloak roles each have unique permissions that apply to users
assigned to a group or to multiple groups.

  - **Roles** are permission-centric. Roles apply permissions to users.

  - **Groups** are user-centric. They are a collection of users. Use
    groups to manage users.

Menu options differ depending on the role you are assigned. For example,
a user assigned only the Operator role cannot view the **Service
Manager**, **Activate a Service**, or **Application Settings** menus.

ViNO provides four roles that correspond to different permissions.
<span style="background: #c0c0c0">Table 1</span> defines the roles and
their permissions.

**Table <span id="Table_1" style="background: #c0c0c0">1</span>. ViNO Keycloak Roles
and Permissions**

<table>
<tbody>
<tr class="odd">
<td><p>Keycloak Role</p></td>
<td><p>Permissions</p></td>
</tr>
<tr class="even">
<td><p><strong>administrator</strong></p></td>
<td><ul>
<li><p>Change settings in Settings Management.</p></li>
<li><p>View service details on the homepage.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>designer</strong></p></td>
<td><ul>
<li><p>Create and modify flows in Service Manager.</p></li>
<li><p>Activate services.</p></li>
<li><p>View Settings Management, but cannot edit the screen.</p></li>
<li><p>View service details on the homepage.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>provisioner</strong></p></td>
<td><ul>
<li><p>Activate and deactivate services.</p></li>
<li><p>View Settings Management, but cannot edit the screen.</p></li>
<li><p>View service details on the homepage.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>operator</strong></p></td>
<td><p>View service details on the homepage. This role is read-only.</p></td>
</tr>
<tr class="even">
<td><p><strong>user</strong></p></td>
<td><p>Required role that provides basic access permissions to ViNO.</p>
<ol>
<li><p>All users must be assigned this role in addition to at least one of the other four roles.</p></li>
</ol></td>
</tr>
</tbody>
</table>

<span id="Table_2" style="background: #c0c0c0">Table 2</span> provides a matrix of
task-to-role permissions.
**Table <span style="background: #c0c0c0">2</span>. Keycloak
Task-to-Role Permissions**

<table>
<thead>
<tr class="header">
<th><p>Task</p></th>
<th><p>Description</p></th>
<th><p>administrator</p></th>
<th><p>designer</p></th>
<th><p>provisioner</p></th>
<th><p>operator</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>View Main Menu</p></td>
<td><p><br />
</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
</tr>
<tr class="even">
<td><p>View Service Manager</p></td>
<td><p><br />
</p></td>
<td><p>––</p></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
<tr class="odd">
<td><p>View Service Activation Menu</p></td>
<td><p><br />
</p></td>
<td><p>––</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
</tr>
<tr class="even">
<td><p>View Application Settings Menu</p></td>
<td><p><br />
</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
<tr class="odd">
<td><p>View Settings Management Menu</p></td>
<td><p><br />
</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
<tr class="even">
<td><p>View User Management Menu</p></td>
<td><p><br />
</p></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
<tr class="odd">
<td><p>View Help Menu</p></td>
<td><p><br />
</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
</tr>
<tr class="even">
<td><p>View Installed Docker Containers Details</p></td>
<td><p><br />
</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>View Web Service Documentation</p></td>
<td><p><br />
</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
</tr>
<tr class="even">
<td><p>GET /rest/services</p></td>
<td><p>Returns a list of registered ViNO services.</p></td>
<td><p>––</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
</tr>
<tr class="odd">
<td><p>GET /rest/services/{serviceId}/template</p></td>
<td><p>Returns a template for activating the ViNO service with the given service ID.</p></td>
<td><p>––</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
</tr>
<tr class="even">
<td><p>POST /rest/services/{serviceId}/activate</p></td>
<td><p>Activates a ViNO service with the given service ID. Requires the template for the same service to be provided as the POST body.</p></td>
<td><p>––</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
</tr>
<tr class="odd">
<td><p>GET /rest/services/{serviceId}/status/{jobId}</p></td>
<td><p>Returns the status of a service activation using the given service ID and job ID.</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
</tr>
<tr class="even">
<td><p>GET /rest/services/{serviceId}/cancel/{jobId}</p></td>
<td><p>Issues a cancellation request to a currently activating ViNO service with the given service ID and job ID.</p></td>
<td><p>––</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
</tr>
<tr class="odd">
<td><p>GET /rest/services/activationlog/{jobId}</p></td>
<td><p>Returns the activation log for a ViNO service with the given job ID.</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
</tr>
<tr class="even">
<td><p>DELETE /rest/services/{serviceId}/deactivate/{jobId}</p></td>
<td><p>Deactivates a ViNO service with the given service ID and job ID. If a deactivation flow is present in the service, it executes.</p></td>
<td><p>––</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
</tr>
<tr class="odd">
<td><p>GET /rest/services/activated</p></td>
<td><p>Returns a list of all ViNO service activations.</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
</tr>
<tr class="even">
<td><p>GET /rest/services/activated/{jobId}</p></td>
<td><p>Returns the data for a ViNO service activation with the given job ID.</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>POST /rest/service/activated</p></td>
<td><p>Registers a ViNO service activation. This occurs automatically after a service has finished activating, and should not be called manually.</p></td>
<td><p>––</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
</tr>
<tr class="even">
<td><p>POST /rest/service/activated/{jobId}</p></td>
<td><p>Updates a ViNO service activation using the given job ID. This occurs automatically while a service is activating, and should not be called manually.</p></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
<tr class="odd">
<td><p>POST /rest/service/activated/{jobId}/{visible}</p></td>
<td><p>Toggles the visibility of a ViNO service activation in the Service Activations table on the ViNO homepage.</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
</tr>
<tr class="even">
<td><p>POST /rest/service/register</p></td>
<td><p>Registers a new ViNO service. This occurs automatically when services are saved in the Service Manager, and should not be called manually.</p></td>
<td><p>––</p></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
<tr class="odd">
<td><p>DELETE /rest/service/unregister/{serviceId}</p></td>
<td><p>Unregisters a ViNO service using the given service ID. This occurs automatically when services are deleted in the Service Manager, and should not be called manually.</p></td>
<td><p>––</p></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
<tr class="even">
<td><p>GET /rest/settings/all</p></td>
<td><p>Returns a list of settings saved in Settings Management.</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
<tr class="odd">
<td><p>GET /rest/settings/system</p></td>
<td><p>Returns a list of ViNO system settings (currently unused).</p></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
<tr class="even">
<td><p>GET /rest/settings/system/{key}</p></td>
<td><p>Returns a ViNO system setting with the given key (currently unused).</p></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
<tr class="odd">
<td><p>GET /rest/settings/group/{name}</p></td>
<td><p>Returns a settings group from Settings Management using the given name.</p></td>
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
<tr class="even">
<td><p>POST /rest/settings/group</p></td>
<td><p>Saves a new settings group and its contents to Settings Management. If the group already exists, the new content is merged.</p></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
<tr class="odd">
<td><p>POST /rest/settings/defaults</p></td>
<td><p>Saves a new default settings group and its contents to Settings Management. If the group already exists, the new content is merged.</p></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
<tr class="even">
<td><p>POST /rest/settings/replace</p></td>
<td><p>Saves a new settings group and its contents to Settings Management. If the group already exists, it is replaced with the new content.</p></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
<tr class="odd">
<td><p>POST /rest/settings/system</p></td>
<td><p>Saves a new ViNO system setting (currently unused).</p></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
<tr class="even">
<td><p>DELETE /rest/settings/deleteRootGroup/<br />
{rootGroupName}</p></td>
<td><p>Deletes a settings root group from Settings Management with the given root group name.</p></td>
<td><ul>
<li></li>
</ul></td>
<td><p>––</p></td>
<td><p>––</p></td>
<td><p>––</p></td>
</tr>
</tbody>
</table>

  
  

### Populating the Keycloak Realm for ViNO

To populate the Keycloak realm for ViNO, you need to add and configure a
role, group, user, and client. Refer to the following sections for
information on completing these tasks.

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Adding
    Roles in Keycloak</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Adding
    a Group in Keycloak</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Adding
    a User in Keycloak</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Adding
    a ViNO Client in Keycloak</span></span>

#### Adding Roles in Keycloak

The following roles must be added in Keycloak. The roles must be added
exactly as shown below for ViNO to function correctly.

  - <span style="text-decoration: none"><span style="background: #c0c0c0">user</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">operator</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">provisioner</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">designer</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">administrator</span></span>

To add roles:

1.  Click on the Roles menu, and then click **Add Role**.

2.  Enter **user** in the **Role Name** field.

3.  Click Save to create the **user** role.

4. Repeat steps 1-3 to create four additional roles: **operator**,
    **provisioner**, **designer**, and **administrator**.

#### Adding a Group in Keycloak

Creating a group in Keycloak enables you to manage users. **Groups** are
*user-centric*. They are a collection of users. For example, you may
want to create a group named Administrators, which has been mapped to
the administrator role. Then you would assign users to the new
Administrators group to give them administrator permissions.

**NOTE** Each ViNO group must contain the **user** role, which provides basic
    access permissions.

To add a group:

1.  Select the **Groups** menu, and then click **New**.

2.  Enter a group name in the **Name** field. Unlike roles, specific
    names for groups are not required.

3.  Click Save to create the new group.

4. Select the **Role Mappings** menu.

5. Select roles from the **Available Roles** menu.

6. Click **Add Selected** to assign the roles to the new group. For example, you could add the **user** and the **administrator** roles
    to a new group. See
    <span style="text-decoration: none"><span style="background: #c0c0c0">Table
    1</span></span> for a description of user roles and permissions.

#### Adding a User in Keycloak

This section describes how to add a new user to Keycloak.

To add a user:

1.  Click the **Users** menu, and then click **Add User**.

2.  Enter the new username in the **Username** field.

3.  Change the **Email Verified** setting from Off to On to disable
    sending an email to the new user.

4.  Click Save to save the new user.

5. Click the **Credentials** tab to configure a temporary password for
    the new user.

6. (Optional) Change the **Temporary** setting to Off to disable
    requiring the new user to change the default password at login.

7. Enter a password, confirm it, and click **Reset Password** to
    configure the new password.

8. Click the **Groups** tab, and then select the new **** group (that
    was previously created) from the **Available Groups** menu.

9. Click Join to add the new user to the selected group.

#### Adding a ViNO Client in Keycloak

Adding a client to Keycloak enables ViNO to request Keycloak to
authenticate users.

To add a client:

1.  Click the **Clients** menu, and then click Create.

2. Enter **vino-api** in the **Client ID** field, and then click Save
    to create the **vino-api** client.

3. Under the **Access Type** drop-down, select **Confidential**.

4. Type * in the **Valid Redirect URIs** field and in the **Web
    Origins** field, then click Save.

5. Click the **Credentials** tab to view the generated client secret.

6. Copy the value in the vino-api client **Secret** field for use in
    step 3 in
    <span style="text-decoration: none"><span style="background: #c0c0c0">Initializing
    ViNO</span></span>.

## Initializing ViNO

To initialize ViNO:

1.  Run the command **./initialize.sh** using the command line in the
    /opt/vino/vino-docker directory.

2. Press Enter when the script prompts for Vino Name, Default route,
    and Keycloak host.

3. When the script prompts for the Keycloak client secret, paste the
    **vino-api** client secret that you copied in step 6 in
    <span style="text-decoration: none"><span style="background: #c0c0c0">Adding
    a ViNO Client in Keycloak</span></span>, and then press Enter.

4. Press Enter for the remaining prompts. ViNO completes the
    initialization.

5. The next prompt enables you to add a signing certificate to the ViNO
    set of accepted CA certificates to securely communicate with
    upstream and downstream services: **Would you like to add an
    additional Root CA Certificate to the ViNO Node Runtime? (Yes/No)**

    Select:
    
      - **Yes** to add a signing certificate to facilitate SSL
        communications (such as, HTTPS or LDAPS).
    
      - **No** to bypass this option.

6. When the initialize.sh script has finished running, open a browser
    and enter the IP address of your ViNO host in the URL bar. This step
    navigates to the ViNO Login screen.

## Logging in to ViNO

To log in to ViNO:

1.  In the **Authentication Required** screen, click Authenticate.

2. In the **Log In** screen, enter the username and password that you
    created when generating the Keycloak realm, then click Log In. ViNO
    displays a blank homepage as shown below.

    ![Figure_1](Virtual%20Network%20Orchestrator%20\(ViNO\)%20Installation%20Guide_html_6843aca5d59b1884.png)
    
    **Caution**: To avoid being logged out after 10 minutes while working in
    the Service Manager, you must open the Service Manager in a separate
    window. If you only have the Service Manager open, you are logged out of
    ViNO after 10 minutes with no warning. Even after being logged out, it
    appears that you can work and save in the Service Manager, but your
    changes are not saved.

3. Refer to the [Virtual Network Orchestrator (ViNO) User Guide](USER.MD) for
    information on using ViNO.

<div title="footer">

  

</div>
