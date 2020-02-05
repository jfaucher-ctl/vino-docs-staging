<div title="header">

  

</div>

<div id="TextSection" dir="ltr">

<span class="sd-abs-pos" style="position: absolute; top: 0in; left: 0in; width: 343px">![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_ecc8317a0e8f7dff.png)
</span>Virtual Network Orchestrator (ViNO) User Guide

Software Version 1.0.1

February 4, 2020

  
  

  
  

©2020 CenturyLink. All Rights Reserved. The CenturyLink mark, pathways
logo and certain CenturyLink product names are the property of
CenturyLink. All other marks are the property of their respective
owners.

  
  

  
  

</div>

<div id="Table of Contents1" dir="ltr">

<div id="Table of Contents1_Head" dir="ltr">

**Contents**

</div>

[Introduction](#Introduction)

[ViNO Software Components](#ViNO-Software-Components)

[ViNO Keycloak Roles and Groups](#ViNO-Keycloak-Roles-and-Groups)

[ViNO Homepage](#ViNO-Homepage)

[Accessing Keycloak Account
Settings](#Accessing-Keycloak-Account-Settings)

[Service Activations and Service Detail
Sections](#Service-Activations-and-Service-Detail-Sections)

[Displaying Service Details](#Displaying-Service-Details)

[Deactivating a Service](#Deactivating-a-Service)

[Reactivating a Service](#Reactivating-a-Service)

[Displaying and Hiding Service
Entries](#Displaying-and-Hiding-Service-Entries)

[Activating a Service](#Activating-a-Service)

[Application Settings Menu–Settings
Management](#Application-Settings-Menu–Settings-Management)

[Using Settings Categories](#Using-Settings-Categories)

[Adding a Settings Category](#Adding-a-Settings-Category)

[Modifying the Display Name in a Settings
Category](#Modifying-the-Display-Name-in-a-Settings-Category)

[Using Groups](#Using-Groups)

[Adding a Group](#Adding-a-Group)

[Modifying the Display Name for a
Group](#Modifying-the-Display-Name-for-a-Group)

[Using Scalars](#Using-Scalars)

[Adding a Scalar](#Adding-a-Scalar)

[Modifying a Scalar](#Modifying-a-Scalar)

[Using Scalar Lists](#Using-Scalar-Lists)

[Adding a Scalar List](#Adding-a-Scalar-List)

[Modifying the Display Name for a Scalar
List](#Modifying-the-Display-Name-for-a-Scalar-List)

[Downloading and Uploading a JSON
File](#Downloading-and-Uploading-a-JSON-File)

[Downloading a JSON File](#Downloading-a-JSON-File)

[Uploading a JSON File](#Uploading-a-JSON-File)

[Deleting Elements](#Deleting-Elements)

[Application Settings–User
Management](#Application-Settings–User-Management)

[Service Manager](#Service-Manager)

[Service Manager Components](#Service-Manager-Components)

[Service Manager Concepts](#Service-Manager-Concepts)

[Creating or Cloning a Project](#Creating-or-Cloning-a-Project)

[Creating a Project](#Creating-a-Project)

[Cloning a Project Repository](#Cloning-a-Project-Repository)

[Saving a Project](#Saving-a-Project)

[Working in the Service Designer](#Working-in-the-Service-Designer)

[Working in the Palette](#Working-in-the-Palette)

[Managing Nodes in the Palette
Manager](#Managing-Nodes-in-the-Palette-Manager)

[Accessing the Palette Manager](#Accessing-the-Palette-Manager)

[Managing Nodes](#Managing-Nodes)

[Adding Nodes to the Palette](#Adding-Nodes-to-the-Palette)

[Using Built-In or Third-Party Node-RED
Nodes](#Using-Built-In-or-Third-Party-Node-RED-Nodes)

[Working with Flow Tabs](#Working-with-Flow-Tabs)

[Adding a Flow Tab](#Adding-a-Flow-Tab)

[Editing Flow Tab Properties](#Editing-Flow-Tab-Properties)

[Enabling or Disabling a Flow Tab](#Enabling-or-Disabling-a-Flow-Tab)

[Deleting a Flow Tab](#Deleting-a-Flow-Tab)

[Switching Between Flows](#Switching-Between-Flows)

[Working with Nodes](#Working-with-Nodes)

[Using the Inject Node](#Using-the-Inject-Node)

[Using the Debug Node](#Using-the-Debug-Node)

[Using the Function Node](#Using-the-Function-Node)

[Using the Change Node](#Using-the-Change-Node)

[Using the Switch Node](#Using-the-Switch-Node)

[Using the Template Node](#Using-the-Template-Node)

[Using ViNO Nodes](#Using-ViNO-Nodes)

[Using Conditional Start and Conditional End
Nodes](#Using-Conditional-Start-and-Conditional-End-Nodes)

[Adding Status Messages to Built-In
Nodes](#Adding-Status-Messages-to-Built-In-Nodes)

[Using the Function Node to Manipulate
Parameters](#Using-the-Function-Node-to-Manipulate-Parameters)

[Working with Wires](#Working-with-Wires)

[Moving Wires](#Moving-Wires)

[Deleting Wires](#Deleting-Wires)

[Working with Subflows](#Working-with-Subflows)

[Designing a Subflow](#Designing-a-Subflow)

[Working with Messages](#Working-with-Messages)

[Changing Message Properties](#Changing-Message-Properties)

[Using the Service Status Node](#Using-the-Service-Status-Node)

[Working with the Sidebar](#Working-with-the-Sidebar)

[Using Parameters](#Using-Parameters)

[Configuring Parameters on Nodes](#Configuring-Parameters-on-Nodes)

[Editing Parameters](#Editing-Parameters)

[Using Parameter Mapping](#Using-Parameter-Mapping)

[Using Parameter Mappings and
Conditionals](#Using-Parameter-Mappings-and-Conditionals)

[Using Parameter Wrapper Injection and
Extraction](#Using-Parameter-Wrapper-Injection-and-Extraction)

[Using Parameter Combiner Modes](#Using-Parameter-Combiner-Modes)

[Passing Parameters Between a Parent Flow and
Subflow](#Passing-Parameters-Between-a-Parent-Flow-and-Subflow)

[Using Loops](#Using-Loops)

[Using Basic Loops](#Using-Basic-Loops)

[Considerations for Each Loop](#Considerations-for-Each-Loop)

[Using Input Parameters in a Loop
Step](#Using-Input-Parameters-in-a-Loop-Step)

[Using Parameter Mapping and Loops](#Using-Parameter-Mapping-and-Loops)

[Using Parallel Execution](#Using-Parallel-Execution)

[Joining Parallel Branches](#Joining-Parallel-Branches)

[Creating a Service Deactivation
Flow](#Creating-a-Service-Deactivation-Flow)

[Error Handling](#Error-Handling)

[Using the Catch Node](#Using-the-Catch-Node)

[Using the Throw Node](#Using-the-Throw-Node)

[Adding Rollback Capability](#Adding-Rollback-Capability)

</div>

List of Tables

<div id="Table of Figures1" dir="ltr">

[Table 1. ViNO Components](#Table-1)

[Table 2. ViNO Keycloak Roles and Permissions](#Table-2)

[Table 3. ViNO Homepage Navigation Bar](#Table-3)

[Table 4. Service Activations Section](#Table-4)

[Table 5. Service Details Field Descriptions](#Table-5)

[Table 6. Service Activation Screen](#Table-6)

[Table 7. Settings Management Screen](#Table-7)

[Table 8. New Scalar Field Descriptions](#Table-8)

[Table 9. Service Manager Components](#Table-9)

[Table 10. Service Manager Concepts](#Table-10)

[Table 11. ViNO Nodes](#Table-11)

[Table 12. Property Edit Window](#Table-12)

</div>

<div id="Table of Figures2" dir="ltr">

[Figure 1. ViNO Homepage](#Figure-1)

[Figure 2. Service Activation Screen](#Figure-2)

[Figure 3. Service Activation Details Screen](#Figure-3)

[Figure 4. Settings Management Screen](#Figure-4)

[Figure 5. JSON Upload and Download Buttons](#Figure-5)

[Figure 6. Service Manager Screen](#Figure-6)

[Figure 7. Service Manager Screen in a New ViNO](#Figure-7)

[Figure 8. Filter Node Field and Toggle Palette](#Figure-8)

[Figure 9. User Settings Window](#Figure-9)

[Figure 10. User Settings–Nodes List in Palette Tab](#Figure-10)

[Figure 11. Palette Install Tab](#Figure-11)

[Figure 12. Service Manager Flow Tab Navigation Bar](#Figure-12)

[Figure 13. Edit Flow Sidebar](#Figure-13)

[Figure 14. Example of Using the Conditional Start Node](#Figure-14)

[Figure 15. Example of Using the Conditional End Node](#Figure-15)

[Figure 16. Example of Using Conditional Start and Conditional End
Nodes](#Figure-16)

[Figure 17. Working with Wires](#Figure-17)

[Figure 18. Dropping a Node on a Wire](#Figure-18)

[Figure 19. Create Subflow Option](#Figure-19)

[Figure 20. Example of New Subflow and Toolbar](#Figure-20)

[Figure 21. Subflow Example](#Figure-21)

[Figure 22. Service Manager Sidebar](#Figure-22)

[Figure 23. Property Edit Window](#Figure-23)

[Figure 24. Edit Input Parameter Window](#Figure-24)

[Figure 25. Mode Field in Property Edit Window](#Figure-25)

[Figure 26. Using a Parameter Wrapper Node](#Figure-26)

[Figure 27. Example of a Basic Loop](#Figure-27)

[Figure 28. Using Input List in a Loop](#Figure-28)

[Figure 29. Loop Start Node Example](#Figure-29)

[Figure 30. Example of Creating a Parallel Branch](#Figure-30)

[Figure 31. Example of Joining Parallel Branches](#Figure-31)

[Figure 32. Example of Join Node Properties](#Figure-32)

[Figure 33. Service with Corresponding Deactivation Flow](#Figure-33)

[Figure 34. Deactivation Flow Example](#Figure-34)

[Figure 35. Implementing a Rollback](#Figure-35)

</div>

  

# Introduction

This document describes how to use the Virtual Network Orchestrator
(ViNO) to develop services and flows in order to:

  - Create, activate, deactivate, and manage virtual services on
    OpenStack, NFVi platforms, and servers

  - Manage virtual service network interfaces

  - Use ViNO nodes to interact with OpenStack controllers in order to
    manipulate Virtual Machines (VMs)

  - Interact with servers using robust Ansible support

In addition to this guide, ViNO documentation includes the *Virtual
Network Orchestrator (ViNO) Installation Guide*, which describes how to
install and initialize a ViNO instance and how to create a realm in
Keycloak. ViNO uses [Keycloak](https://www.keycloak.org/) for
authentication.

ViNO enables you to create, activate, deactivate, and manage virtual
services for:

  - Servers

  - Firewalls

  - Routers

  - SD WANs

ViNO is built on
<span style="text-decoration: none">[Node-RED](https://nodered.org/)</span>,
which is a browser-based editor for wiring together flows using a wide
range of nodes in the palette that can be deployed to its runtime in a
single click.

**NOTE:** The Node-RED site contains detailed information and user
documentation on using the product. The expectation is for ViNO users to
use the <span style="text-decoration: none">[Node-RED
documentation](https://nodered.org/docs/)</span> to familiarize
themselves with the product functionality before using ViNO to create
service flows.

ViNO builds on the flow-based model provided in Node-RED by including
the following components specific to creating, configuring, and
delivering services:

  - VNF-specific nodes that enable you to define how data is passed
    between the steps within in a flow.

  - A backing web service API that enables new nodes to provide
    interfaces to complex network management actions.

  - A management user interface.

  - An authentication abstraction.

  - Drivers that provide access to the Netconf protocol, Ansible, and
    the OpenStack V3 API.

  - REST APIs that provide a unified and consistent interface for
    managing the full life cycle of service activation, deactivation,
    and management.

The additional nodes included in the software enhance the functionality
of Node-RED by enabling ViNO to programmatically and automatically
generate activation templates that have full compatibility with existing
Node-RED default nodes, as well as many of the community-contributed
nodes available on the internet.

**NOTE: **The difference between a ViNO service and a Node-RED flow is
that a ViNO service must always start with a **service entrypoint** node
and end with a **service endpoint** node.

# ViNO Software Components

The ViNO software is comprised of several components as described in
<span id="Table-1" style="background: #c0c0c0">Table 1</span>.

**Table <span style="background: #c0c0c0">1</span>. ViNO Components**

<table>
<tbody>
<tr class="odd">
<td><p>Component</p></td>
<td><p>Description</p></td>
</tr>
<tr class="even">
<td><p><strong>NGINX</strong></p></td>
<td><p>A lightweight, high performance HTTP proxy, load balancer, and web host. In the ViNO software suite, NGINX serves the role of an HTTP reverse proxy to expose select services inside a local private network and access them from the Docker host system.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Service Manager</strong></p></td>
<td><p>A combination of an unmodified Node-RED installation and a custom user interface on top. The Node-RED instance has been branded for CenturyLink and includes several <span style="text-decoration: none"><span style="background: #c0c0c0">custom</span></span> nodes that provide the ability to create service flows that can be activated programmatically and registered with an API instance.</p></td>
</tr>
<tr class="even">
<td><p><strong>ViNO API</strong></p></td>
<td><p>An Express.js-based REST interface that provides service registration, activation, history, and status monitoring as well as hosts several protocol drivers that enable the Service Manager to interact with remote devices using Netconf, Ansible, and Openstack APIs.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Settings Server</strong></p></td>
<td><p>Provides a hierarchical data store that enables users to define groups of settings and variables.</p></td>
</tr>
<tr class="even">
<td><p><strong>Keycloak Authentication Server</strong></p></td>
<td><p>ViNO uses the <span style="text-decoration: none"><a href="https://www.keycloak.org/">Keycloak</a></span> authentication server to provide local authentication and the ability to incorporate federated authentication methods such as Kerberos or LDAP. In addition, ViNO can use Single Sign On (SSO) Identity Providers (IdPs) over SAML or OpenID Connect (OIDC).</p>
<p>This component alleviates the need to log into each individual piece of the ViNO software suite. It also simplifies the process of integrating the open source projects that comprise ViNO into the corporate authentication mechanisms.</p></td>
</tr>
<tr class="odd">
<td><p><strong>PostgreSQL Database</strong></p></td>
<td><p>ViNO uses a PostgreSQL database to store various pieces of information such as the configuration for authentication and the history of activations including service input and output.</p></td>
</tr>
</tbody>
</table>

# ViNO Keycloak Roles and Groups

ViNO Keycloak roles each have unique permissions that apply to users
assigned a role or multiple roles.

  - **Roles** are permission-centric. Roles apply permissions to users.

  - **Groups** are user-centric. They are a collection of users. Use
    groups to manage users.

Menu options differ depending on the role you are assigned. For example,
a user assigned only the operator role cannot view the **Service
Manager**, **Activate a Service**, or **Application Settings** menus.

ViNO provides four roles that correspond to different permissions.
<span id="Table-2" style="background: #c0c0c0">Table 2</span> defines
the roles and their permissions.

**Table <span style="background: #c0c0c0">2</span>. ViNO Keycloak Roles
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
<ol start="3">
<li><p>All users must be assigned this role in addition to at least one of the other four roles.</p></li>
</ol></td>
</tr>
</tbody>
</table>

  
  

## ViNO Homepage

The menu options on the homepage navigation bar differ depending on the
role
(<span style="text-decoration: none"><span style="background: #c0c0c0">administrator</span></span>,
<span style="text-decoration: none"><span style="background: #c0c0c0">designer</span></span>,
<span style="text-decoration: none"><span style="background: #c0c0c0">operator</span></span>,
or
<span style="text-decoration: none"><span style="background: #c0c0c0">provisioner</span></span>)
your username is assigned. For example, a user assigned only the
**operator** role cannot view the **Service Manager**, **Activate a
Service**, and **Application Settings** menus.

<span id="Table-3" style="background: #c0c0c0">Table 3</span> describes
the menus located in the top navigation bar of the homepage.
<span style="text-decoration: none"><span style="background: #c0c0c0">Figure
1</span></span> shows an example of the homepage.

**Table <span style="background: #c0c0c0">3</span>. ViNO Homepage
Navigation Bar**

<table>
<thead>
<tr class="header">
<th><p>Menu</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Main</strong> <strong>–</strong> <strong>Homepage</strong></p></td>
<td><p>Displays the <strong>Service Activations</strong> and the <strong>Service Detail</strong> sections. Click <strong>Main</strong> to refresh or return to the homepage.</p></td>
</tr>
<tr class="even">
<td><p><strong>Service Manager</strong></p></td>
<td><p>Displays the flow editing tool (<strong>Service Manager</strong>). Click ViNO-Service Manager to return to the home page.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Activate a Service</strong></p></td>
<td><p>Enables you to select a service from the drop-down, enter customer information, and then progress through the configuration steps to activate the service.</p></td>
</tr>
<tr class="even">
<td><p><strong>Application Settings</strong></p></td>
<td><p>Includes the following options:</p>
<ul>
<li><p><strong>Settings Management</strong> – Enables you to add, remove, or modify settings categories and modify default scalar values and overrides. See <span style="text-decoration: none"><span style="background: #c0c0c0">Application Settings Menu–Settings Management</span></span>.</p></li>
<li><p><strong>User Management</strong> – Enables you to access the Keycloak Admin console. See Application Settings–User Management.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Help</strong></p></td>
<td><p>Includes:</p>
<p><strong>Installed Docker Containers Details</strong> – Displays the installed version of each ViNO component: vino-core, vino-database, vino-keycloak, and<br />
vino-proxy.</p>
<p><strong>Web Service Documentation</strong> – Displays the ViNO REST services in Swagger. If you build software to call ViNO, use this option for a machine-to-machine interface. Use the browser Back button to return to the ViNO home page.</p></td>
</tr>
<tr class="even">
<td><p><em>Username</em></p>
<p>(Displays the name of the user who is logged in)</p></td>
<td><p>Includes the <strong>Account Settings</strong> menu and the Log Out button.</p>
<ul>
<li><p><strong>Account Settings</strong> menu – Provides access to Keycloak. See <span style="text-decoration: none"><span style="background: #c0c0c0">Accessing Keycloak Account Settings</span></span>.</p></li>
<li><p>Log Out button – Click to log out of ViNO.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Accessing Keycloak Account Settings

The **Account Settings** option (in the *username* drop-down) enables
you to access the Keycloak account manager. Keycloak displays the **Edit
Account** screen by default and pre-populates your username in the
**Username** field. The navigation bar at the top of the screen
includes:

  - **English** – Default language. Click the drop-down to select a
    different language that applies to the options in the **Account
    Settings** menu.

  - **Back to vino-api** – Returns you to the ViNO homepage.

  - **Sign Out** – Logs you out of Keycloak and ViNO.

The **Edit Account** screen includes the following options. Refer to the
<span style="text-decoration: none">[Keycloak](https://www.keycloak.org/)</span>
documentation for information on using these options.

  - **Account**

  - **Password**

  - **Authenticator**

  - **Sessions**

  - **Applications**

# Service Activations and Service Detail Sections

The homepage contains the following two sections, which are read-only:

  - **Service Activations** – Enables a designer or provisioner to
    deactivate and reactivate services.

  - **Service Detail** – Enables all users to view service details and
    details for the specific steps in a service. See
    <span style="text-decoration: none"><span style="background: #c0c0c0">Displaying
    Service Details</span></span>.

The **Service Activations** section lists active and deactivated
services. To filter the list of entries, enter criteria in the Search
field (you do not have to click Enter). Search criteria applies to the
data in all columns. Clear the criteria to re-display all entries.

<span style="background: #c0c0c0">Figure 1</span> shows an example of
the homepage. To display information in the **Service Detail** section
for a specific service, highlight the entry in the **Service
Activations** section.

**Figure <span id="Figure-1" style="background: #c0c0c0">1</span>. ViNO
Homepage**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_6843aca5d59b1884.png)

<span id="Table-4" style="background: #c0c0c0">Table 4</span> describes
the buttons and columns in the **Service Activations** section. Each
column can be toggled to list the entries in either alphabetical or
numerical order (ascending or descending).

**Table <span style="background: #c0c0c0">4</span>. Service Activations
Section**

<table>
<tbody>
<tr class="odd">
<td><p>Component</p></td>
<td><p>Description</p></td>
</tr>
<tr class="even">
<td><p><strong>Deactivate Button</strong></p></td>
<td><p>Deactivates a service. Highlight the service entry in the <strong>Services</strong> section and click Deactivate. See <span style="text-decoration: none"><span style="background: #c0c0c0">Deactivating a Service</span></span>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Reactivate Button</strong></p></td>
<td><p>Reactivates a service. Highlight the service entry in the <strong>Services</strong> section and click Reactivate. See <span style="text-decoration: none"><span style="background: #c0c0c0">Reactivating a Service</span></span>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Show All Activations</strong></p>
<p><br />
<br />
</p>
<p><strong>Filter All Activations</strong></p></td>
<td><p>Displays all activations (service entries) irrespective of the <strong>Visible in UI</strong> column setting (Yes or No).</p>
<p>Hides service entries that have the <strong>Visible in UI</strong> column set to Yes.</p>
<p>See <span style="text-decoration: none"><span style="background: #c0c0c0">Displaying and Hiding Service Entries</span></span>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Search Field</strong></p></td>
<td><p>Filter the list of entries. Search criteria applies to data in all columns. When the Search field is blank, ViNO displays all entries. When the Search field contains criteria, ViNO displays only those entries that match the search criteria. Clear the criteria to re-display all entries.</p></td>
</tr>
<tr class="even">
<td><p><strong>Service Name Column</strong></p></td>
<td><p>Name of the service as defined in the associated flow.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Customer Name</strong></p></td>
<td><p>Name of the customer associated with the service as defined in the associated flow.</p></td>
</tr>
<tr class="even">
<td><p><strong>Settings Root</strong></p></td>
<td><p>Identifies the root group to use for all constants in the service activation.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Status</strong></p></td>
<td><p>Status of the service (Activated or Terminated).</p></td>
</tr>
<tr class="even">
<td><p><strong>Completed At</strong></p></td>
<td><p>Date and time stamp when the service activation or deactivation was completed. The time stamp is UTC (Coordinated Universal Time).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Activation Log</strong></p></td>
<td><p>Configuration log of a service activation. Click Close to close the log or click Download Log to open and save the file.</p></td>
</tr>
<tr class="even">
<td><p><strong>Visible in UI Column</strong></p></td>
<td><p>Displays (Yes) or hides (No) an entry. The default is Yes. See <span style="text-decoration: none"><span style="background: #c0c0c0">Displaying and Hiding Service Entries</span></span>.</p></td>
</tr>
</tbody>
</table>

## Displaying Service Details

The **Service Detail** section displays information about a service and
about each step in the flow. This information is historical and is
helpful for troubleshooting. To display information for a service,
select the service in the **Services** section.

<span id="Table-5" style="background: #c0c0c0">Table 5</span> describes
the fields in the **Service Detail** section.

**Table <span style="background: #c0c0c0">5</span>. Service Details
Field Descriptions**

<table>
<tbody>
<tr class="odd">
<td><p>Field</p></td>
<td><p>Description</p></td>
</tr>
<tr class="even">
<td><p><strong>Job ID</strong></p></td>
<td><p>Identifier for the service Activation log. ViNO automatically assigns and updates the job ID.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Customer Name</strong></p></td>
<td><p>Name of the customer associated with the service as defined in the <strong>Customer Info</strong> section when you activate a service (<strong>Service Activation</strong> screen).</p></td>
</tr>
<tr class="even">
<td><p><strong>Settings Root</strong></p></td>
<td><p>Identifies the root group to use for all constants in the service activation.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Activation Status</strong></p></td>
<td><p>Displays the value listed in the <a href="#UsingtheVirtualNetworkOrchestrator(ViNO"><strong>Status</strong></a> column (<strong>Service Activations</strong> section).</p></td>
</tr>
<tr class="even">
<td><p><strong>Activation Notes</strong></p></td>
<td><p>Notes associated with the service as defined in the <strong>Customer Info</strong> section when you activate a service (<strong>Service Activation</strong> screen).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Select Step for Details</strong></p></td>
<td><p>Drop-down that lists each step in a flow as defined by the designer.</p></td>
</tr>
<tr class="even">
<td><p><strong>Input Parameters </strong></p>
<p>and</p>
<p><strong>Output Parameters</strong></p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
</p></td>
<td><p>Select an entry from the <strong>Select Step for Details</strong> drop-down to display the Input <strong></strong> and <strong></strong> Output parameters defined by the designer for that specific node. Both parameter sections include the following columns:</p>
<ul>
<li><p><strong>Parameter Name</strong> – Name of the parameter defined in the flow.</p></li>
<li><p><strong>Parameter Description</strong> – Description of the parameter defined in the flow.</p></li>
<li><p><strong>Parameter Type</strong> – Type of parameter (for example, string, Boolean, number, enumeration) defined in the flow.</p></li>
<li><p><strong>Parameter Value</strong> – Value of the parameter defined in the flow.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Deactivating a Service

When you deactivate a service, ViNO tears down the service
configuration, but retains the configuration information enabling you to
easily reactivate the service if needed.

**NOTE: **A flow must have a deactivation path defined to in order to
deactivate the service.

To deactivate a service:

1.  Select the service that you want to deactivate.

2.  Click Deactivate. ViNO displays a confirmation window.

3.  Click OK to proceed with deactivating the service. The Deactivate
    Service log opens and displays the progress. When the process is
    complete, the last entry in the log displays: Service deactivation
    completed successfully.

4.  Click OK to close the log. ViNO updates the service status to
    Terminated.

## Reactivating a Service

To reactivate a service:

1.  Select the service that you want to reactivate.

2.  Click Reactivate. ViNO displays a confirmation window.

3.  Click OK to proceed with reactivating the service. The Activating
    Service log opens and displays the progress. When the process is
    complete, the last entry in the log displays: Service activation
    completed successfully.

4.  Click OK to close the log. ViNO adds a new activation entry to the
    **Service Activations** section.

## Displaying and Hiding Service Entries

The **<span style="background: #c0c0c0">Visible in UI </span>**column
(homepage \> **Services** section) enables you to display or hide
service entries. The default setting is Yes (display an entry). To hide
an entry, change the setting to No. To display all entries irrespective
of the entry setting, click Show All Activations. To hide entries that
are set to No, click the button, which changes to Filter Activations.

## Activating a Service

The **Activate a Service** menu displays the **Service Activation**
screen, which enables a user assigned the
<span style="text-decoration: none"><span style="background: #c0c0c0">administrator</span></span>
or the
<span style="text-decoration: none"><span style="background: #c0c0c0">provisioner</span></span>
role to select a service to be activated.
<span id="Table-6" style="background: #c0c0c0">Table 6</span> describes
the sections and fields in the **Service Activation** screen.

**Table <span style="background: #c0c0c0">6</span>. Service Activation
Screen**

<table>
<thead>
<tr class="header">
<th><p>Section</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Service Info</strong></p></td>
<td><p>Includes the <strong>Service Name</strong> and the <strong>Description</strong> fields, which ViNO populates.</p></td>
</tr>
<tr class="even">
<td><p><strong>Customer Info</strong></p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
</p></td>
<td><p>Includes the following fields:</p>
<ul>
<li><p><strong>Settings Root</strong> – (Required) Select the root group to use for all constants in the service activation.</p></li>
<li><p><strong>Customer Name</strong> – Enter the customer name associated with the service.</p></li>
<li><p><strong>Notes</strong> – Enter specific information about the service.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Service Steps</strong></p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
</p></td>
<td><p>Lists the steps in a flow that are required to create a service. Select a node to display its parameters (default, custom, or pre-configured).</p>
<p>Each node includes the following fields:</p>
<ul>
<li><p><strong>Name</strong> – Name of the node as entered by the designer.</p></li>
<li><p><strong>Node ID</strong> – System-generated unique identifier.</p></li>
<li><p><strong>Description</strong> – Text entered by the designer in the Edit panel of a node.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Parameters</strong></p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
</p></td>
<td><p>Displays parameters assigned by a designer for each node in a flow.</p>
<ul>
<li><p><strong>Show Pre-Configured Parameters</strong><span style="font-weight: normal"> </span>– Displays node parameters that have<br />
pre-assigned values. To enter or update a parameter, double-click the field. A field can still be updated when it is greyed-out. To cancel an update, refresh the browser (which returns you to the home page).</p></li>
<li><p><strong>Hide Pre-Configured Parameters</strong> – Displays parameters (with or without assigned values) that apply to a node and hides parameters displayed by the <strong>Show Pre-Configured Parameters</strong> setting.</p></li>
</ul>
<ol start="5">
<li><p>When a parameter has the <strong>Final</strong> checkbox selected (located in the <strong>Edit Input Parameter</strong> window), it is not displayed in the <strong>Parameter</strong> section in order to protect the integrity of a finalized flow. Parameters that have the <strong>Final</strong> checkbox selected can only be updated from the <strong>Edit Input Parameter</strong> window.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td><p>Back Button</p></td>
<td><p>Displays parameters for the previous service step.</p></td>
</tr>
<tr class="even">
<td><p>Next Button</p></td>
<td><p>Displays parameters for the next service step.</p></td>
</tr>
</tbody>
</table>

  
  

To activate a service:

1.  Select a service from the **Service** drop-down (**Activate a
    Service** menu). ViNO auto-populates the **Service Name** and the
    **Description** fields with the information that was entered when
    the flow was created. <span style="background: #c0c0c0">Figure
    2</span> shows the Create NBS VM service selected with information
    populated in the **Details** section.

**NOTE: **ViNO only auto-populates the **Service** drop-down with
services that start with a **service entrypoint** node.

**Figure <span id="Figure-2" style="background: #c0c0c0">2</span>.
Service Activation Screen**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_ec7d72dc221e2e34.png)

  
  

2.  Click Select Service. The **Service Activation Details** screen
    displays the **Services Info**, **Customer Info**, and the **Service
    Steps** sections as shown in
    <span style="text-decoration: none"><span style="background: #c0c0c0">Figure
    3</span></span>.

3.  Select an entry from the **Settings Root** drop-down (**Customer
    Info** section). The Settings Root identifies the root group to use
    for all constants in the service activation. ViNO populates the
    values in this  
    drop-down from the Settings Management entries.

4.  (Optional) Enter the customer name in the **Customer Name** field.
    If you do not enter a name, ViNO auto-populates the value as *ViNO*.

5.  (Optional) Enter notes pertaining to the customer or site (for
    example, site address) in the **Notes** field.

6.  Select each step (or click the Next button) to display parameters
    for each step (**Service Steps** section). The parameters for each
    step correspond to a node in the flow (that contains values).

7.  Populate parameters as needed by toggling through each step.
    Required fields are highlighted in red text and change to green text
    when you enter a value. Pre-populated variables appear greyed out in
    the **Service Activation** screen. To override a default value,
    double-click the field and confirm that you want to override the
    value, then enter the new value.

8.  After you have toggled through each step, click Next to display the
    **Review and Activate** screen. This screen displays the service
    name, description, and the steps including their parameters (see
    <span style="background: #c0c0c0">Figure 3</span>).

To activate a service without first checking the parameters for each
step, select the last step in the flow, and then click Activate. In the
**Review and Activate** screen, click Activate. If a step is missing a
required parameter, an error message is displayed at the top of the
screen.

**Figure <span id="Figure-3" style="background: #c0c0c0">3</span>.
Service Activation Details Screen**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_343fc50256973c63.png)  
![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_c619db600e916b46.png)  
  
  

9.  To proceed with activating the service, click Activate. To include
    ViNO debug messages in the activation log, select the **Run in Debug
    Mode** checkbox, then click Activate. To make additional changes to
    parameters, click Edit Service Parameters to return to the **Service
    Activation** screen.

When you click Activate, ViNO displays the following warning message:

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_fc719ca388a0572c.png)

10. Click Activate to activate the service. ViNO displays a status log
    as shown below.

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_b67481da3e830a02.png)

11. Click OK at the end of the status log to close the window.

# Application Settings Menu–Settings Management

The **Settings Management** screen (**Application Settings** menu)
enables you to create, group, and store settings, elements, and scalars
that can be used in services. Storing elements can provide variable
default values to driver nodes. For example, a service may call for a
different VM image or size based on the needs of a customer. The
**Settings Management** screen enables you to store a group of settings
that defines images and sizes, which can be passed in at service
activation time rather than having to manually configure them each time
or hard coding them into the flow.

To use constants in a ViNO service, see
<span style="text-decoration: none"><span style="background: #c0c0c0">Constants</span>.</span>

The following sections describe each element in Settings Management:

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Settings Categories</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Groups</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Scalars</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Scalar Lists</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Downloading
    and Uploading a JSON File</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Deleting
    Elements</span></span>

**NOTE: **Only a user assigned the administrator role can edit and save
values in the **Settings Management** screen. A user assigned the
designer role can only view the **Settings Management** screen. If a
designer updates this screen and tries to save the changes, an error
message is displayed and the changes are not saved.

A new instance of ViNO does not include categories. You must create them
manually or create them by loading the data using a JSON file. Settings
management data is stored in JSON files. See
<span style="text-decoration: none"><span style="background: #c0c0c0">Downloading
and Uploading a JSON File</span></span>.

An example of the **Settings Management** screen with three expanded
categories is shown in <span style="background: #c0c0c0">Figure
4</span>. Element names that are preceded with an asterisk ( **\*** )
are default elements. When you select an element, a window displays
information for that element including options to add a group, a scalar
list, or a scalar. If the element you select contains additional
elements (such as groups, scalars, or scalar lists), the tree expands to
display all the elements.

**Figure <span id="Figure-4" style="background: #c0c0c0">4</span>.
Settings Management Screen**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_e3d750596bb7ff45.png)

  
  

<span id="Table-7" style="background: #c0c0c0">Table 7</span> describes
the section and buttons on the **Settings Management** screen.

**Table <span style="background: #c0c0c0">7</span>. Settings Management
Screen**

|                         |                                                                                                                                                  |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| Element                 | Description                                                                                                                                      |
| **Settings Categories** | Top level element in **Settings Management**. Categories can contain groups, scalars, and scalar lists, which are displayed in a tree structure. |
| **Add Category**        | Add a new category.                                                                                                                              |
| **Upload JSON File**    | Load settings data from a JSON file to an instance of ViNO.                                                                                      |
| **Download JSON File**  | Select and save categories to a JSON file. Use this file to load your saved categories to a new instance of ViNO.                                |
| **Apply Button**        | Apply and save changes made to elements.                                                                                                         |
| **Add Group**           | Add a group to an element.                                                                                                                       |
| **Add Scalar List**     | Add a scalar list, which functions similarly to a group except that you can only add scalars. Scalar lists do not allow groups to be added.      |
| **Add Scalar**          | Add values used in services.                                                                                                                     |

## Using Settings Categories

When you create a settings category, ViNO automatically creates a
Defaults group and names it with the category display name. Each group
that is added inherits the values from the initial Defaults group.
Defaults groups cannot be deleted. However, you can add groups, scalars,
and scalar lists to a Defaults group. Elements added to a Defaults group
are automatically inherited by all groups for that category. Default
values are identified by an asterisk ( **\*** ).

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Adding
    a Settings Category</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Modifying
    the Display Name in a Settings Category</span></span>

### Adding a Settings Category

To add a new settings category:

1.  Click Add Category. A window displays that enables you to enter
    values in the following fields:

<!-- end list -->

  - **Name** – Category name that is displayed in service definitions or
    during service activation. A name must be one word and can consist
    of letters, numbers, and hyphens. The **Name** field is a unique
    identifier and once set, cannot be changed.

  - **Display Name** – Category name that is displayed in the UI (such
    as, the **Settings** screen and the **Service Activation** screen)
    to provide a display-friendly and readable name for the category.
    The **Display Name** field can contain multiple words (including
    letters, numbers, spaces, and hyphens).

<!-- end list -->

2.  Click Apply to save the new category.

### Modifying the Display Name in a Settings Category

To modify the display name for a category:

1.  Highlight the category in the **Settings Categories** section.
    Highlighting a category expands the tree in addition to displaying
    information related to that category.

2.  Click in the **Display Name** field, and then overwrite the existing
    name with the new name.

3.  Click Apply.

## Using Groups

Groups are used to store other groups, scalars, and scalar lists. Groups
are similar to categories, but they do not contain their own Defaults
group.

Attributes for groups include:

  - **Name** – Name that is displayed in service definitions or during
    service activation. A name must be one word and can consist of
    letters, numbers, and hyphens. The **Name** field is a unique
    identifier and once set, cannot be changed.

  - **Display Name** – Name that is displayed in the UI (such as, the
    **Settings** screen and the **Service Activation** screen) to
    provide a display-friendly and readable name for the group. The
    **Display Name** field can contain multiple words (including
    letters, numbers, spaces, and hyphens).

Refer to the following sections for information on using groups:

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Adding
    a Group</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Modifying
    the Display Name for a Group</span></span>

### Adding a Group

To add a new group:

1.  Select a category or group in the tree. The properties window for
    that element is displayed.

2.  Click the Add Group button. Alternatively, you can right-click a
    category or group and select Add \> Group.

3.  Enter a name in the **Name** field.

4.  Enter a name in the **<span style="background: #c0c0c0">Display Name
    </span>**field.

5.  Click Apply to save the new group.

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_8869a559bdda76a5.png)

### Modifying the Display Name for a Group

To modify the display name for a group:

1.  Select the group in the tree to open the **Group** window.

2.  Click in the **Display Name** field, and then overwrite the existing
    name with the new name. For example:  
    ![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_44ab52e352f68e87.png)

3.  Click Apply to save your changes.

## Using Scalars

Scalars contain values that are used by ViNO services. Scalars can
contain string, Boolean, or number values. You can also designate these
values as required for service activation.

Scalars that are added to a:

  - Defaults group are inherited by all groups.

  - Non-default groups override inherited default scalars with the same
    name.

Refer to the following sections for information on using scalars:

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Adding
    a Scalar</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Modifying
    a Scalar</span></span>

### Adding a Scalar

To add a new scalar:

1.  Select a category, group, or scalar list in the tree, and then click
    Add Scalar. Alternatively, right-click on an element and select Add
    \> Scalar.

2.  Enter values in the **Name**, **Display Name**, **Required**,
    **Type**, and **Value** fields.

3.  Click Apply to save the new scalar. For example:

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_7b5fa4f20d1f883a.png)

<span id="Table-8" style="background: #c0c0c0">Table 8</span> describes
the fields in the New Scalar window.

**Table <span style="background: #c0c0c0">8</span>. New Scalar Field
Descriptions**

|                  |                                                                                                                                                                                                                                                           |
| ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Field            | Description                                                                                                                                                                                                                                               |
| **Name**         | Scalar name that is displayed in service definitions and during service activation. A name must be one word and can consist of letters, numbers, and hyphens. The Name field is a unique identifier and once set, cannot be changed.                      |
| **Display Name** | Scalar name that is displayed in the **Settings** screen and the **Service Activation** screen to provide a display-friendly and readable name for the category. This field can contain multiple words (including letters, numbers, spaces, and hyphens). |
| **Required**     | Determines whether a field is required (True) or optional (False). Select the appropriate option from the drop-down.                                                                                                                                      |
| **Type**         | Determines the value for the scalar. Select **String**, **Number**, or **Boolean** from the drop-down as appropriate.                                                                                                                                     |
| **Value**        | Value used by a ViNO service that references this scalar. The type of value that can be entered in this field is determined by the setting in the **Type** field for this scalar.                                                                         |

### Modifying a Scalar

To modify a scalar:

1.  Select the scalar in the tree. The values for the scalar attribute
    are displayed. The name in the **Name** field for a scalar is a
    unique identifier and once set, cannot be changed.

2.  Enter changes by backspacing over existing values or by selecting a
    value from a drop-down.

3.  Click Apply to save your changes. To cancel changes, refresh the
    page.

## Using Scalar Lists

Scalar lists enable you to categorize and store scalars. While scalars
are not required to be stored in a scalar list, you may want to organize
certain scalars together. For example, environment variables related to
a specific system or a set of systems that share common architecture,
such as the IP address, SSH username, SSH key, and password for a given
system.

Scalar lists function similarly to a group except that you can only add
scalars. Scalar lists do not allow groups to be added.

Refer to the following sections for information on managing scalar
lists:

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Adding
    a Scalar List</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Modifying
    the Display Name for a Scalar List</span></span>

### Adding a Scalar List

To add a new scalar list:

1.  Select a category or group in the tree. The properties window for
    the selected element is displayed.

2.  Click Add Scalar List. Alternatively, right-click the selected
    element and select **Add** \> **Scalar List**.

3.  Enter values in the
    <span style="text-decoration: none"><span style="background: #c0c0c0">Name</span></span>
    and the **<span style="background: #c0c0c0">Display Name
    </span>**fields in the **New Scalar List** window.

4.  Click Apply to save the new scalar list.

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_98d5cb8c333c33c.png)

### Modifying the Display Name for a Scalar List

To modify the display name for a scalar list:

1.  Click the scalar list in the tree. The scalar list properties window
    is displayed.

2.  Click in the **Display Name** field, and then overwrite the existing
    name with the new name.

3.  Click Apply to save your changes. To cancel the change, refresh the
    page.

## Downloading and Uploading a JSON File

ViNO enables you to save elements into a JSON file and then upload the
file to another ViNO. <span style="background: #c0c0c0">Figure 5</span>
shows the JSON file buttons on the **Settings Management** screen.

**Figure <span id="Figure-5" style="background: #c0c0c0">5</span>. JSON
Upload and Download Buttons**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_d21dc0f41cbfde7d.png)

  
Refer to the following sections for information on using JSON files:

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Downloading
    a JSON File</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Uploading
    a JSON File</span></span>

### Downloading a JSON File

Downloading enables you to save elements to a JSON file and then upload
the file to another instance of ViNO.

To save elements to a JSON file:

1.  Click the **Download JSON File** button (see
    <span style="text-decoration: none"><span style="background: #c0c0c0">Figure
    5</span></span>). A window opens enabling you to select which
    elements to save to a JSON file.

2.  Navigate to the element you wish to save and select it.

3.  Click Download.

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_466d1b3259302b5.png)

4.  In the **Opening vino-settings.json** window:

<!-- end list -->

1.  Select the **vino-settings.json** checkbox. This is the default
    name. You can change this name as needed after the file is saved.

2.  Select the action the browser should take.

<!-- end list -->

  - In Firefox, save the file to a location or open it.

  - In Chrome, the filename appears in the bottom left of the screen.
    Click the down arrow to open the file or display it in your Download
    folder.

### Uploading a JSON File

Uploading a JSON file enables you to re-use previously saved elements in
a settings category.

To upload a JSON file:

1.  Click the **Upload JSON File** button (see
    <span style="text-decoration: none"><span style="background: #c0c0c0">Figure
    5</span></span>). The **Select a file to load** window is displayed.

2.  Click Choose File, and then navigate to the location of the JSON
    file you wish to upload.

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_d4457eeaf82a99de.png)

3.  Select the file and then click Open. The file is displayed.

4.  Scroll to the bottom of the file and click **Upload**. The new
    elements are uploaded and displayed in the **Settings Categories**
    section.

## Deleting Elements

**Caution**: All elements stored within a deleted settings category,
group, scalar, or scalar list are also deleted. This process cannot be
undone and the deleted values cannot be retrieved. Default groups cannot
be deleted directly, but are deleted if the category is deleted.

To delete a settings category, group, scalar, or scalar list:

1.  Right-click the element in the tree.

2.  Select the Delete option. A warning confirmation message is
    displayed and requires you to confirm the action. The following
    example shows the confirmation message to delete the scalar list
    *LML Test*:

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_821bcc31d541d2a4.png)

3.  Click Delete to delete the element.

# Application Settings–User Management

The **User Management** option (**Application Settings** menu) opens the
Keycloak homepage where you can access the Admin Console and the
<span style="text-decoration: none">[Keycloak](https://www.keycloak.org/)</span>
documentation.

# Service Manager

The **Service Manager** enables a
<span style="text-decoration: none"><span style="background: #c0c0c0">Error:
Reference source not found</span></span> to create reusable network
services by designing flows that represent the steps required to create
a service. The main difference between a ViNO service and a Node-RED
flow is that a ViNO service must always start with a
<span style="text-decoration: none"><span style="background: #c0c0c0">service
entrypoint</span></span> **** node and end with a
<span style="text-decoration: none"><span style="background: #c0c0c0">service
endpoint</span></span> node.

**NOTE: **The term *flow* is used for a single set of connected nodes
and for the tabs in the Service Manager, which can contain multiple
flows (sets of connected nodes). A *project* includes all the flow tabs
and subflows in the Service Manager.

The underlying technology is Node-RED with several additions to:

  - Interact with Openstack.

  - Configure services using Ansible and Netconf.

  - Define how data is passed between steps within a flow.

ViNO can also leverage the nodes built in to Node-RED as well as an
array of third-party nodes developed by the Node-RED community.

**Caution**: To avoid being logged out after 10 minutes while working in
the Service Manager, you must open the Service Manager in a separate
window. If you only have the Service Manager open, you are logged out of
ViNO after 10 minutes with no warning. Even after being logged out, it
appears that you can work and save in the Service Manager, but your
changes are not saved.

<span style="background: #c0c0c0">Figure 6</span> shows a partial
**Service Manager** screen that has the Ansible Hostname tab displayed.

**Figure <span id="Figure-6" style="background: #c0c0c0">6</span>.
Service Manager Screen**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_e33856283105831.png)

  
To display a description of a node in the Palette, hover your cursor
over it.

To return to the homepage, click VINO-Service Manager located in the top
left of the **Service Manager** screen.

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_cb9e7beaa13e9d3.png)

## Service Manager Components

<span id="Table-9" style="background: #c0c0c0">Table 9</span> describes
the components on the **Service Manager** screen.

**Table <span style="background: #c0c0c0">9</span>. Service Manager
Components**

<table>
<thead>
<tr class="header">
<th><p>Component</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Save icon<br />
</strong><img src="img/Virtual%20Network%20Orchestrator%20User%20Guide_html_27180e5a1db62da7.png" width="95" height="32" /></p></td>
<td><p>Saves all flows for the project. This icon briefly changes into a loading icon during the process of saving the flows.</p></td>
</tr>
<tr class="even">
<td><p><strong>Menu icon<br />
</strong><img src="img/Virtual%20Network%20Orchestrator%20User%20Guide_html_1cfaf1dd65136967.png" width="48" height="35" /></p>
<p><br />
</p></td>
<td><p>Drop-down that includes the following options:</p>
<p><strong>Projects</strong>, <strong>View</strong>, <strong>Import</strong>, <strong>Export</strong>, <strong>Search Flows</strong>, <strong>Configuration Nodes</strong>, <strong>Flows</strong>, <strong>Subflows</strong>, <strong>Manage Palette</strong>, <strong>Setting</strong>, <strong>Keyboard Shortcuts</strong>, <strong>Node-RED Website</strong>, and <em>Node-RED software version</em>. Refer to the <span style="text-decoration: none"><a href="https://nodered.org/docs/">Node-RED documentation</a> </span>for information on these options.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Designer workspace</strong></p></td>
<td><p>Create flows in this space.</p></td>
</tr>
<tr class="even">
<td><p><strong>Right sidebar</strong></p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
<br />
</p>
<p><br />
</p></td>
<td><p>Includes the following informational displays. See <span style="text-decoration: none"><span style="background: #c0c0c0">Working with the Sidebar</span>.</span></p>
<ul>
<li><p><img src="img/Virtual%20Network%20Orchestrator%20User%20Guide_html_1957778097a5cabb.png" width="50" height="38" /> <strong>info</strong> – Displays information for the node currently highlighted.</p></li>
<li><p><img src="img/Virtual%20Network%20Orchestrator%20User%20Guide_html_a210f1321179cb26.png" width="46" height="39" /> <strong>history</strong> – Displays the history of your changes and enables you to revert or push changes to a Git repository.</p></li>
<li><p><img src="img/Virtual%20Network%20Orchestrator%20User%20Guide_html_3f6ceb07ca7cb0d9.png" width="46" height="40" /> <strong>debug</strong> – Displays debug messages from the <strong>debug</strong> node.</p></li>
<li><p><img src="img/Virtual%20Network%20Orchestrator%20User%20Guide_html_bf88d74fcadfd287.png" width="39" height="40" /> Informational drop-down that includes the following options. When you select an option, its icon is added to the sidebar.</p></li>
</ul>
<ul>
<li><p><strong>Node information</strong> – Same description as the <strong>info</strong> icon.</p></li>
<li><p><strong>Project history</strong> – Same description as the <strong>history</strong> icon.</p></li>
<li><p><strong>Debug messages</strong> – Same description as the <strong>debug</strong> icon.</p></li>
<li><p><strong>Configuration nodes</strong> –N/A.</p></li>
<li><p><strong>Context data</strong> – N/A.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Node palette</strong></p></td>
<td><p>Located in the left panel of the screen. Includes the node categories listed below.</p></td>
</tr>
<tr class="even">
<td><p>subflows</p></td>
<td><p>Set of connected nodes that can be reused within a larger flow. A subflow is represented as a single node in the workspace that can be opened in a tab to display the underlying flow. The <strong>subflow</strong> node category does not exist until a subflow is created.</p></td>
</tr>
<tr class="odd">
<td><p>input</p></td>
<td><p>Includes nodes that cover the basic communications mechanisms that applications are likely to use. The nodes range from UDP and TCP to the higher-level HTTP and the publish/subscribe MQTT (Message Queuing Telemetry Transport).</p></td>
</tr>
<tr class="even">
<td><p>output</p></td>
<td><p>Essentially the mirror images of the basic set of input nodes that provide a way to send data on the same set of protocols (for example, MQTT, HTTP, UDP).</p></td>
</tr>
<tr class="odd">
<td><p>function</p></td>
<td><p>Nodes that carry out specific processing functions. Functions range from the simple <strong>delay</strong> and <strong>switch</strong> nodes to the programmable <strong>function</strong> node that can be adapted to most programming needs.</p></td>
</tr>
<tr class="even">
<td><p>social</p></td>
<td><p>Basic social media nodes that support interaction with email and Twitter. These nodes enable flows to send or receive email or to send or receive tweets.</p></td>
</tr>
<tr class="odd">
<td><p>storage</p></td>
<td><p>Targeted at devices such as the Raspberry Pi. This category is limited and focuses on file-based storage.</p></td>
</tr>
<tr class="even">
<td><p>analysis</p></td>
<td><p>Performs standard analyses on incoming messages. The only node provided is the <strong>sentiment</strong> node, which can be used to try to determine the sentiment of an incoming message based on the words used in the message (for example, an email or a tweet).</p></td>
</tr>
<tr class="odd">
<td><p>advanced</p></td>
<td><p>Miscellaneous nodes offering various types of functionality.</p></td>
</tr>
<tr class="even">
<td><p>ViNO</p></td>
<td><p>Nodes used to create ViNO services.</p>
<p>The additional nodes included in the software enhance the functionality of Node-RED by enabling ViNO to programmatically and automatically generate activation templates that have full compatibility with existing<br />
Node-RED default nodes, as well as many of the community-contributed nodes available on the internet.</p></td>
</tr>
<tr class="odd">
<td><p>Raspberry Pi</p></td>
<td><p>Nodes specific to Raspberry Pi usage.</p></td>
</tr>
<tr class="even">
<td><p>abacus</p></td>
<td><p>Nodes used to create web services with Node-RED.</p></td>
</tr>
</tbody>
</table>

## Service Manager Concepts

The Service Manager enables you to access the designer functionality to
create nodes and flows.
<span id="Table-10" style="background: #c0c0c0">Table 10</span>
describes the concepts of the Service Manager functionality.

**Table <span style="background: #c0c0c0">10</span>. Service Manager
Concepts**

| Concept                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Flow**               | Describes a single set of connected nodes. Click the <span style="background: #c0c0c0">Save </span>icon to save a flow. This term is also used to describe a tab in the Service Manager, which can contain multiple flows (sets of connected nodes).                                                                                                                                                                                                                                                        |
| **Parent Flow**        | A parent flow contains subflows.                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Flow (Tab)**         | A flow is represented as a tab at the top of the Service Manager workspace and is the main way to organize nodes. Use the **Project History** option (<span style="text-decoration: none"><span style="background: #c0c0c0">Informational drop-down</span></span>) to save all flow tabs and subflows in the Service Manager (known as a *project*).                                                                                                                                                        |
| **Project**            | Includes all the flow tabs and subflows in the Service Manager for the active project. Only one project may be active at a time.                                                                                                                                                                                                                                                                                                                                                                            |
| **Subflow**            | A subflow is a collection of nodes that are collapsed into a single node in the workspace. You can use subflows to reduce some visual complexity of a flow or to package a group of nodes as a reusable component used in multiple places. See <span style="text-decoration: none"><span style="background: #c0c0c0">Working with Subflows</span></span>.                                                                                                                                                   |
| **Workspace**          | The Workspace is the main area where you develop flows by dragging nodes from the palette and wiring them together. The workspace has a row of tabs along the top; one for each flow and subflow. See <span style="text-decoration: none"><span style="background: #c0c0c0">Working in the Service Designer</span></span>.                                                                                                                                                                                  |
| **Node**               | A node is the basic building block of a flow. Nodes are triggered by either receiving a message from the previous node in a flow or by waiting for an external event, such as an incoming HTTP request or a timer. A node processes the message or event and then may send a message to the next node in the flow. A node can have only one input port and as many output ports as it requires. See <span style="text-decoration: none"><span style="background: #c0c0c0">Working with Nodes</span></span>. |
| **Configuration Node** | A **config** node is a special type of node that holds reusable configuration that can be shared by regular nodes in a flow. **Config** nodes do not appear in the main workspace, but can be seen by opening the Configuration Nodes option in the <span style="background: #c0c0c0">Menu </span>icon drop-down (next to the Save button). See <span style="text-decoration: none"><span style="background: #c0c0c0">Working with the Sidebar</span></span>.                                               |
| **Message**            | Messages are passed between the nodes in a flow. They are plain JavaScript objects that can have a set of properties. Messages are often referred to as **msg** within the editor. See <span style="text-decoration: none"><span style="background: #c0c0c0">Working with Messages</span></span>.                                                                                                                                                                                                           |
| **Wire**               | Wires connect the nodes and represent how messages pass through the flow. See <span style="text-decoration: none"><span style="background: #c0c0c0">Working with Wires</span></span>.                                                                                                                                                                                                                                                                                                                       |

## Creating or Cloning a Project

When you access the Service Manager on a new ViNO, you are presented
with the options to create a project or clone an existing project from a
Git repository. Cloning a repository maps your ViNO to the correct Git
repository used to save your projects.

<span style="background: #c0c0c0">Figure 7</span> shows the **Service
Manager** screen in a new ViNO.

**Figure <span id="Figure-7" style="background: #c0c0c0">7</span>.
Service Manager Screen in a New ViNO**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_f5223aa706958124.png)

Refer to the following sections for information on creating and cloning
projects:

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Creating
    a Project</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Cloning
    a Project Repository</span></span>

### Creating a Project

To create a new Node-RED project:

1.  Click Create Project.

2.  Enter your username and email for your Git repository in the **Setup
    your version control client** window. Both fields are required.

3.  Click Next.

4.  Enter your project name (required) and an optional description in
    the **Create your project** window.

5.  Click Next.

6.  (Optional) You can configure a name for your flow file and
    credentials file that will be uploaded to your repository in the
    **Create your project files** window.

7.  Click Next.

8.  (Optional) You can provide a custom encryption key to protect the
    project files in your repository in the **Setup encryption of your
    credentials file** window.

9.  Click Create Project. A success message is displayed.

10. Click Done.

### Cloning a Project Repository

Cloning a repository maps your ViNO to the correct Git repository used
to save your projects.

To clone a repository:

1.  Click Clone Repository (See
    <span style="text-decoration: none"><span style="background: #c0c0c0">Figure
    7</span></span>).

2.  Enter your username and email for your Git repository in the **Setup
    your version control client** window. Both fields are required.

3.  Click Next.

4.  Enter the following values in the **Clone a project** window. All
    fields except for the credentials encryption key are required.

<!-- end list -->

1.  Your project name.

2.  Repository URL for the project you wish to clone.

3.  Enter your username and password for your Git repository.

4.  Enter the credentials encryption key.

5.  Click Clone Project. The project is loaded.

## Saving a Project

It is likely that the services you develop on your instance of ViNO will
need to be deployed or shared with other ViNO instances. Therefore, it
is important to save the flows that you create so they can be
transferred easily between ViNO instances. Use the Project History icon
or option in the
<span style="text-decoration: none"><span style="background: #c0c0c0">Informational
drop-down</span></span> to save flow tabs and subflows by pushing the
changes to a Git repository. This option also enables you to revert
changes instead of saving them.

When you clone a Git repository, your ViNO Service Manager maps directly
to a Git repository to provide a version control system for saving
projects. The Git repository mapping is done when you clone a repository
on a new instance of ViNO.

**Caution**: Do not use the **Import** or **Export** options
(<span style="background: #c0c0c0">Menu </span>icon drop-down) to share
or save a project. These functions lose parameter mappings. See
<span style="text-decoration: none"><span style="background: #c0c0c0">Using
Parameter Mapping</span></span>.

# Working in the Service Designer

The main workspace is where you develop service flows by dragging nodes
from the palette and wiring them together. The workspace has a row of
tabs along the top: one for each flow and subflow that is open.

The footer of the workspace includes buttons to zoom in and out as well
as the ability to reset the default zoom level. The footer also includes
a toggle button for the view navigator. The view provides a scaled down
view of the entire workspace that highlights the area currently visible.
You can drag this area around the navigator to quickly jump to other
parts of the workspace. You can also customize the workspace view using
the **View** tab in the **User Settings** window
(<span style="background: #c0c0c0">Menu </span>icon \> **Settings**
option).

Refer to the following sections for information on using the workspace
components.

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Working
    in the Palette</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Managing
    Nodes in the Palette Manager</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Working
    with Flow Tabs</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Working
    with Nodes</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Working
    with Wires</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Working
    with Subflows</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Working
    with Messages</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Working
    with the Sidebar</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Parameters</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Loops</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Parallel Execution</span></span>

## Working in the Palette

The Palette is located on the left of the Service Manager workspace and
lists nodes (by section) that are available to use in flows. Nodes are
organized into categories, with inputs, outputs and functions listed at
the top. Subflows (when they exist) appear in a category at the top of
the palette. Click a category to expand or collapse the node list.

Above the palette is the **filter nodes** field that enables you to
search for nodes. To hide the entire palette, click the Toggle Palette
arrow as shown in <span style="background: #c0c0c0">Figure 8</span>.

**Figure <span id="Figure-8" style="background: #c0c0c0">8</span>.
Filter Node Field and Toggle Palette**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_26542139a43a39bc.png)

  
  

To display a complete description of a node, hover your cursor over it.
You can install additional nodes into the palette using either the
command-line or the Palette Manager. See
<span style="text-decoration: none"><span style="background: #c0c0c0">Managing
Nodes in the Palette Manager</span></span>.

## Managing Nodes in the Palette Manager

The Palette Manager enables you to manage nodes and install new nodes
into the palette. See the following sections for managing nodes:

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Accessing
    the Palette Manager</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Managing
    Nodes</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Adding
    Nodes to the Palette</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Built-In or Third-Party Node-RED Nodes</span></span>

### Accessing the Palette Manager

To access the Palette Manager:

1.  Click the **<span style="background: #c0c0c0">Menu </span>**icon
    drop-down
    (![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_1cfaf1dd65136967.png)
    ).

2.  Select **Manage Palette**.

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_6a822d16672b58e0.png)

The **User Settings** window opens and displays the **Palette** tab by
default as shown <span style="background: #c0c0c0">Figure 9</span>.

**Figure <span id="Figure-9" style="background: #c0c0c0">9</span>. User
Settings Window**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_b6dc38f086dd3e9f.png)

### Managing Nodes

Each entry in the **Nodes** list (<span style="background: #c0c0c0">Menu
</span>icon \> **Settings** option \> **Palette** tab \> **User
Settings** window) displays the name and version of each module (bundled
nodes) in addition to a list of the individual node types the module
provides. Use the Remove, Disable All, and Update buttons as needed to
manage modules.

NOTE: A node that is currently in use cannot be removed or disabled.

<span style="background: #c0c0c0">Figure 10</span> shows the **Nodes**
list **** in the **Palette** tab.

**Figure <span id="Figure-10" style="background: #c0c0c0">10</span>.
User Settings–Nodes List in Palette Tab**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_c0f481483f226283.png)

### Adding Nodes to the Palette

The **Install** button (**Palette** tab) enables you to search for
available modules (bundle of nodes) and install them.

**Caution**: Third party nodes may not be compatible with ViNO if the
nodes do not follow Node-RED standards.

To search for a module, enter its name in the Search field. The search
results display the details of the modules, including when it was last
updated and a link to its documentation.
<span style="background: #c0c0c0">Figure 11</span> shows the **Install**
tab with an arrow pointing to the documentation icon.

To install the module, click Install.

**Figure <span id="Figure-11" style="background: #c0c0c0">11</span>.
Palette Install Tab**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_70d6cf147d535b20.png)

### Using Built-In or Third-Party Node-RED Nodes

As part of a service definition, it may be necessary to incorporate
nodes that are not included with ViNO. While other nodes can be freely
mixed in within ViNO service flows, additional steps may be taken to
make them useful. The output of non-ViNO nodes can only interface with
ViNO input and output parameters using the utility nodes provided with
ViNO (for example, the
<span style="text-decoration: none"><span style="background: #c0c0c0">service
status</span></span>,
<span style="text-decoration: none"><span style="background: #c0c0c0">parameter
wrapper</span></span>, and
<span style="text-decoration: none"><span style="background: #c0c0c0">throw</span></span>
nodes).

Due to limitations in the Node-RED flow activation procedure, not all
third-party nodes function correctly in ViNO service flows. A
third-party node that replaces the message passed into it with its own
object rather than modifying it prevents a service flow from activating
correctly. Consider the implications before you modify the **msg**
object mid-flow to prevent ViNO service failures.

## Working with Flow Tabs

A flow is represented as a tab (a flow tab) within the Service Manager
workspace and is the main way to organize nodes.

NOTE: The term *flow* is used for a single set of connected nodes and
for the tabs in the Service Manager, which can contain multiple flows
(sets of connected nodes). A *project* includes the flow tabs and
subflows in the Service Manager.

<span style="background: #c0c0c0">Figure 12</span> shows seven flow tabs
in the Service Manager workspace.

**Figure <span id="Figure-12" style="background: #c0c0c0">12</span>.
Service Manager Flow Tab Navigation Bar**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_939415c5acb91f5b.png)

  
Double-click a flow tab to open the **Edit Flow** sidebar, which
displays the name, status, and description (if provided) of the flow.
You can enter a description as needed.
<span style="background: #c0c0c0">Figure 13</span> shows an example of
the **Edit Flow** sidebar.

**Figure <span id="Figure-13" style="background: #c0c0c0">13</span>.
Edit Flow Sidebar**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_bd644243ac0df7b0.png)  
  
  

Refer to the following sections for information on managing flow tabs:

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Adding
    a Flow Tab</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Editing
    Flow Tab Properties</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Enabling
    or Disabling a Flow Tab</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Deleting
    a Flow Tab</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Switching
    Between Flows</span></span>

### Adding a Flow Tab

To add a new flow, either click the Plus icon (
![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_d3a7a654292bc793.png)
) in the flow tab navigation bar (see
<span style="text-decoration: none"><span style="background: #c0c0c0">Figure
12</span></span>) or  
double-click any free space in the tab bar. A flow tab can be reordered
by dragging it in the tab bar.

### Editing Flow Tab Properties

To edit the properties for a flow tab or to enable or disable a flow,
double-click the tab in the top bar to open the **Edit Flow** sidebar as
shown in
<span style="text-decoration: none"><span style="background: #c0c0c0">Figure
13</span></span>. Enter a name and description for the flow. The
description can use Markdown syntax for formatting and appears in the
Information sidebar.

To change the status of a flow, toggle the current status in the
**Status** field. If a flow tab is disabled, none of the nodes it
contains are created when the flow tab is deployed.

### Enabling or Disabling a Flow Tab

To enable or disable a flow tab, double-click the tab in the top bar to
open the **Edit Flow** sidebar  
(see
<span style="text-decoration: none"><span style="background: #c0c0c0">Figure
13</span></span>). To change the status, toggle the current status in
the **Status** field.

When a flow tab is disabled, none of the nodes it contains are created
when the flow tab is deployed. For example, if you have an unfinished
flow and save it, the save process fails and displays errors. If you
first disable the flow, you can save successfully.

### Deleting a Flow Tab

To delete a flow tab, click Delete in the **Edit Flow** sidebar. See
<span style="text-decoration: none"><span style="background: #c0c0c0">Figure
13</span></span>.

### Switching Between Flows

To display a list of the available flow tabs, click the
<span style="background: #c0c0c0">Menu </span>icon in the top bar. Click
the flow tab you wish to open. The display only lists flow tabs. It does
not list subflows (even though they are listed in the tab bar).

## Working with Nodes

The Service Manager palette includes a set of nodes that are the basic
building blocks for creating flows. Nodes are joined by wires using
their ports. A node can have only one input port but many output ports.
A port may have a label that is displayed when you hover your mouse over
it. A node may specify labels (for example, the **switch** node shows
the rule that matches the port). You may also customize the name of a
node by double-clicking the icon (in the workspace) and populating the
**Name** field.

When a node has undeployed changes, it displays a blue circle above it.
If there are errors with its configuration, the node displays a red
triangle.

Certain nodes include a button on either the left or right edge. These
buttons enable interactions with the node from within the editor. The
**inject** and **debug** nodes are the only core nodes that have
buttons.

**NOTE: **To display a complete description of a node, hover your cursor
over it in the palette.

Refer to the following sections for information on core nodes:

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    the Inject Node</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    the Debug Node</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    the Function Node</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    the Change Node</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    the Switch Node</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    the Template Node</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    ViNO Nodes</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Conditional Start and Conditional End Nodes</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Adding
    Status Messages to Built-In Nodes</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    the Function Node to Manipulate Parameters</span></span>

### Using the Inject Node

The **inject** node enables you to manually trigger a flow by clicking
the node’s button within the editor. This node can also be used to
automatically trigger flows at regular intervals.

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_f9fc68140bbacbf1.png)

The message sent by the **inject** node can have its payload and topic
properties set. The payload can be set to one of the following types:

  - Flow or global context property value.

  - String, number, Boolean, buffer, or object.

  - Timestamp (in milliseconds) since January 1st, 1970.

### Using the Debug Node

The **debug** node enables you to display messages in the **debug**
sidebar within the editor.

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_782a9dada90347a5.png)

The sidebar provides a structured view of the messages it is sent, which
makes it easy to explore the message. In addition to the message, the
debug sidebar includes information about the time the message was
received and which **debug** node sent it.

A **debug** node can also be configured to send all messages to the
runtime log or to send a short (32 characters maximum) message to the
status text under the **debug** node in a flow. Use the button on the
node to enable or disable its output.

### Using the Function Node

The **function** node enables JavaScript code to be run against the
messages that are passed through it.

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_976993208c47c169.png)

### Using the Change Node

The **change** node enables you to modify the properties of a message
and set context properties without having to resort to a **function**
node.

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_70cf638de2173cc.png)

Each **change** node can be configured with multiple operations that are
applied in order. The available operations are:

  - **Set** – Set a property. The value can be a variety of different
    types (displayed in the drop-down in the node Properties window) or
    can be taken from an existing message or context property.

  - **Change** – Search and replace parts of a message property.

  - **Move** – Move or rename a property.

  - **Delete** – Delete a property.

### Using the Switch Node

The **switch** node enables messages to be routed to different branches
of a flow by evaluating a set of rules against each message.

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_b7f555e32109a4d2.png)

The **switch** node is configured with the property to test, which can
be either a message property or a context property. The node routes a
message to outputs corresponding to matching rules. You can also
configure the **switch** node to stop evaluating rules when it finds one
that matches. There are four types of rules:

  - **Value** rules are evaluated against the configured property.

  - **Sequence** rules can be used on message sequences, such as those
    generated by the **split** node.

  - **JSON Data Expression** rules can be evaluated against the entire
    message and matches if the expression returns a true value.

  - **Otherwise** rules can be used to match if none of the preceding
    rules have matched.

### Using the Template Node

The **template** node enables you to generate text using a message’s
properties to fill out a template.

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_aad9bb1ba882eeae.png)

This node uses the Mustache templating language to generate the result.

### Using ViNO Nodes

<span id="Table-11" style="background: #c0c0c0">Table 11</span>
describes the custom nodes provided with ViNO.

**Table <span style="background: #c0c0c0">11</span>. ViNO Nodes**

<table>
<thead>
<tr class="header">
<th><p>Node</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>service status</strong></p></td>
<td><p>Enables a designer to output arbitrary status messages during activation. Status messages are visible while they are activating and deactivating.</p></td>
</tr>
<tr class="even">
<td><p><strong>conditional end</strong></p></td>
<td><p>Place this node at the end of a conditional branch. Parameters in nodes on conditional branches that need to be accessed by subsequent steps should be defined in the output parameters of this node.</p>
<ol start="12">
<li><p>This node is deprecated and will be removed in a later version.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td><p><strong>conditional start</strong></p></td>
<td><p>Manages a conditional branching of service flow logic. This node provides parameters to define the <span style="text-decoration: none"><span style="background: #c0c0c0">Left Hand Side</span></span> and the <span style="text-decoration: none"><span style="background: #c0c0c0">Right Hand Side</span></span> <strong></strong> operands of a Boolean expression in addition to the operation to perform and the data type of the operands.</p>
<ol start="13">
<li><p>This node is deprecated and will be removed in a later version.</p></li>
</ol></td>
</tr>
<tr class="even">
<td><p><strong>deactivation endpoint</strong></p></td>
<td><p>When the service finishes with the <strong>deactivation endpoint</strong> node, the database elements related to that activation are updated (for example, with status changes).</p></td>
</tr>
<tr class="odd">
<td><p><strong>loop end</strong></p></td>
<td><p>Used to connect back to the input of a loop start node. Place this node at the end of a loop body.</p></td>
</tr>
<tr class="even">
<td><p><strong>loop start</strong></p></td>
<td><p>Manages a loop in the service flow. This node contains the parameter that controls the number of iterations to perform. Each <strong>loop start</strong> must have a matching <strong>loop end</strong> to connect back to the <strong>loop start</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>parameter wrapper</strong></p></td>
<td><p>Enables arbitrary input parameters to map to properties of the <strong>msg</strong> object that is passed to a following node. Parameter wrappers can be used to:</p>
<ul>
<li><p>Inject ViNO parameters into the Node-RED <strong>msg</strong> object.</p></li>
<li><p>Extract attributes from the msg object and convert them into ViNO parameters.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>service endpoint</strong></p></td>
<td><p>When the service finishes with the <strong>service endpoint</strong> node, the database elements related to that activation are updated (for example, with status changes).</p>
<ol start="14">
<li><p>Each ViNO service must end with a <strong>service endpoint</strong> node (unless your service needs to end with a <strong>service failure</strong> node or a <strong>deactivation endpoint</strong> node).</p></li>
</ol></td>
</tr>
<tr class="odd">
<td><p><strong>service entrypoint</strong></p></td>
<td><p>Creates an HTTP end-point for a service.</p>
<p><strong>Note:</strong> Each ViNO service must start with a <strong>service entrypoint</strong> node<strong>.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>service failure</strong></p></td>
<td><p>When the service finishes with the <strong>service failure</strong> node, the database elements related to that activation are updated (for example, with status changes).</p></td>
</tr>
<tr class="odd">
<td><p><strong>throw</strong></p></td>
<td><p>Throws an error. This node is useful when used in conjunction with a <strong>conditional</strong> node to check whether a particular value is valid. This node generates a service failure or a rollback (depending whether a deactivation flow is defined). The <strong>throw</strong> node is typically paired with a <strong>catch</strong> node to facilitate proper error handling.</p></td>
</tr>
<tr class="even">
<td><p><strong>vino driver ansible</strong></p></td>
<td><p>ViNO driver node that performs Ansible operations. This node runs an Ansible playbook on the provided target system. The playbook provided can be templated using the <a href="https://freemarker.apache.org/">Mustache</a> templating syntax. All input parameters on the Ansible node are available for use within the playbook template and can be referenced with {{parameter_key}} anywhere in the playbook.</p>
<p>To use the key-init features of this node with Openstack, you must generate a public and a private SSH key for ViNO to interact with Openstack.</p>
<p>This node enables the use of a private key to authenticate requests against a remote server. For this to work, the private key must be readable by the root user of the vino-core docker container. To accomplish this, place the private key in a docker volume accessible to the vino-core container. The easiest way to do that is after the ViNO services are running, place the private key file in <strong>/var/lib/docker/volumes/&lt;project name&gt;_ViNO-Common/_data/</strong></p>
<p>Files placed in this directory will be available at the path <strong>/opt/vino/common</strong> inside the vino-core container. The <em>project name</em> is the value configured when ViNO was initialized.</p>
<p>The <strong>vino driver ansible</strong> node contains the input parameter <strong>SSH Private Key</strong> that should be configured with the full path to your private key inside the vino-core container. As an option to using the SSH Private Key, you can use the username and password parameters available on this node.</p></td>
</tr>
<tr class="odd">
<td><p><strong>vino driver netconf</strong></p></td>
<td><p>ViNO driver node that performs Netconf operations. This node performs a Netconf get or edit on the provided target system. The node takes in a Netconf template that uses the <a href="https://freemarker.apache.org/">Mustache</a> templating syntax similar to the Ansible node.</p>
<p>To use the key-init features of this node with Openstack, you must generate a public and a private SSH key for ViNO to interact with Openstack.</p>
<p>This node enables the use of a private key to authenticate requests against a remote server. For this to work, the private key must be readable by the root user of the vino-core docker container. To accomplish this, place the private key in a docker volume accessible to the vino-core container. The easiest way to do that is after the ViNO services are running, place the private key file in <strong>/var/lib/docker/volumes/&lt;project name&gt;_ViNO-Common/_data/</strong></p>
<p>Files placed in this directory will be available at the path <strong>/opt/vino/common</strong> inside the vino-core container. The <em>project name</em> is the value configured when ViNO was initialized.</p>
<p>The <strong>vino driver netconf</strong> node contains the input parameter <strong>SSH Key</strong> that should be configured with the full path to your private key inside the vino-core container. As an option to using the SSH Key, you can use the username and password parameters available on this node.</p></td>
</tr>
<tr class="even">
<td><p><strong>vino driver openstack</strong></p></td>
<td><p>ViNO driver node that performs OpenStack operations.</p></td>
</tr>
</tbody>
</table>

  
  

### Using Conditional Start and Conditional End Nodes

In some cases, it may be necessary to only perform actions in a service
under a certain condition. For example, if you need to perform
operations on a VM that may or may not exist, you can use a condition to
determine whether the VM exists.

**NOTE: **The **conditional start** and the **conditional end** nodes
are deprecated and will be removed in a later version.

While setting up conditional logic is possible in a standard Node-RED
instance, ViNO provides the
<span style="text-decoration: none"><span style="background: #c0c0c0">conditional
start</span></span> and the
<span style="text-decoration: none"><span style="background: #c0c0c0">conditional
end</span></span> nodes to simplify this process and make it more
compatible with the concept of input and output parameters. The
**conditional start** node represents the beginning of a conditional
branch of execution. This node includes the following input parameters
that control how the Boolean expression is to be evaluated at activation
time. The **conditional start** node compares the two values in the
**Left Hand Side** and the **Right Hand Side** using the specified
operator and executes one of two paths depending on the result.

  - **Left Hand Side** – Left hand side operand of the expression.

  - **Operation** – Comparison operator to use (equals, less than, less
    than or equal, greater than, greater than or equal).

  - **Operand Data Type** – Data type of the two operands (string,
    number, or Boolean).

  - **Right Hand Side** – Right hand side operand of the expression.

The top output of the node is intended to connect to the steps to take
if the condition evaluates to false while the bottom output connects to
the nodes to activate if it evaluates to true.
<span style="background: #c0c0c0">Figure 14</span> shows an example of
using a **conditional start** node.

**Figure <span id="Figure-14" style="background: #c0c0c0">14</span>.
Example of Using the Conditional Start Node**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_e65f5b727af05afd.png)

The data type of the **Left Hand Side** and the **Right Hand Side** of
input parameters is always **string** and the operand data type
parameter controls which type those values are converted to at runtime.
Therefore, it is important to ensure the values in those parameters are
valid for the configured operand data type. If the values are invalid,
they trigger an error during activation.

**NOTE: **When the operand data type is set to string or Boolean, only
the **eq** (Equals Comparison) operation can be used.

The **conditional start** node also contains a single output parameter
(Evaluation Result) that contains the result of the comparison.

At the end of both the true and false branches, the last nodes in each
branch must be joined back into a single **conditional end** node (shown
in <span style="background: #c0c0c0">Figure 15</span>). This node
provides a clear indication where the conditional branching has ended
and the service resumes a normal path. The **conditional end** node also
serves an important role in
<span style="text-decoration: none"><span style="background: #c0c0c0">parameter
mapping</span></span>.

**Figure <span id="Figure-15" style="background: #c0c0c0">15</span>.
Example of Using the Conditional End Node**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_af208fce7ae4b1d5.png)

  
  

It is a requirement that both branches of the **conditional start** node
eventually connect back to a single **conditional end** node. If only
one of the branches needs to perform actions, the other branch should
have its output connected directly to the **conditional end** node as
shown in <span style="background: #c0c0c0">Figure 16</span>.

**Figure <span id="Figure-16" style="background: #c0c0c0">16</span>.
Example of Using Conditional Start and Conditional End Nodes**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_6fbcdb63e640091a.png)

### Adding Status Messages to Built-In Nodes

It may often be helpful to display status information about operations
being performed by built-in nodes. To display status information, use
the
<span style="text-decoration: none"><span style="background: #c0c0c0">service
status</span></span> node,
<span style="text-decoration: none"><span style="background: #c0c0c0">parameter
mapping</span></span>, and the built-in Mustache templating in the
status message to display information extracted from the node.

The **service status** node enables you to output arbitrary status
messages during activation. The message can use Mustache-style
templating syntax to inject the input parameters defined on this node
into the status message. This is useful for including output data from a
previous step in the status by:

1.  Creating a new input parameter.

2.  Mapping it to a previous node's output.

3.  Referencing it in the **Message** template.

Properties of the message object can also be referenced in the template
by using msg*.nameOfProperty*.

### Using the Function Node to Manipulate Parameters

There may be situations in which parameters need to be manipulated
during an activation. For example, it may be necessary to concatenate
two or more input parameters or perform some arithmetic on a value. This
can be achieved using the **function** node. This node enables you to
write JavaScript functions and directly manipulate the message object
passed in Node-RED.

By injecting parameters into the message object and then accessing them
in a **function** node, you can leverage the power of a full-featured
scripting language to manipulate input parameters. After the parameter
values are manipulated, the parameters can be injected on to the message
object and extracted into an output parameter.

An example to use the **function** node to concatenate objects would be:

var first= 'Jane ';

var last = 'Doe ';

msg\['full\_name '\] = first + ' ' + last;

return msg;

**NOTE: **Within the **function** node the message object is referenced
with **msg**. The original **msg** object (or a copy of that object)
must always be returned at the end of a function. Returning a new object
that lacks information injected into it by the ViNO nodes breaks the
service flow and causes errors in activation.

## Working with Wires

Nodes are wired together by clicking the left-mouse button on a node’s
port, dragging to the destination node, and then releasing the mouse
button as shown in <span style="background: #c0c0c0">Figure 17</span>.

**Figure <span id="Figure-17" style="background: #c0c0c0">17</span>.
Working with Wires**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_546c8e7e83aaa8a2.png)

When you drag a node with both an input and output port over the
mid-point of a wire, the wire is drawn with a dash. If the node is then
dropped, it is automatically inserted into the flow at that point.
<span style="background: #c0c0c0">Figure 18</span> show how to drop a
node on a wire to insert it mid-flow.

**Figure <span id="Figure-18" style="background: #c0c0c0">18</span>.
Dropping a Node on a Wire**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_461670dacb2999cd.png)

### Moving Wires

To disconnect a wire from a port, select the wire by clicking on it,
then press and hold the Shift key when the left-mouse button is pressed
on the port. When you drag the mouse, the wire disconnects from the port
and can be dropped on another port. If you release the mouse button over
the workspace, the wire is deleted.

### Deleting Wires

To delete a wire, select it by clicking on it and then press the Delete
key.

## Working with Subflows

Subflows enable a group of nodes to be packaged into a reusable piece of
logic that is represented as another node in the palette. These subflows
can then be used as part of parent flows. A
<span style="text-decoration: none"><span style="background: #c0c0c0">parent
flow</span></span> is a flow that contains subflows. Conceptually,
subflows are the equivalent of subroutines in traditional programming
languages.

To create a subflow:

1.  Open the Service Manager.

2.  Click the <span style="background: #c0c0c0">Menu </span>icon (see
    <span style="background: #c0c0c0">Figure 19</span>).

3.  Navigate to **Subflows**.

4.  Select **Create Subflow**.

**Figure <span id="Figure-19" style="background: #c0c0c0">19</span>.
Create Subflow Option**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_e82e83da8b578ec7.png)

  
  

This action opens a new tab that is almost identical to a normal flow
tab with the addition of a small tool bar at the top. The tool bar
enables you to:

  - Control the number of inputs and outputs in the subflow.

  - Open a menu to change subflow properties.

<span style="background: #c0c0c0">Figure 20</span> shows a new subflow
(Subflow 1) and the toolbar.

**Figure <span id="Figure-20" style="background: #c0c0c0">20</span>.
Example of New Subflow and Toolbar**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_d9cb5751a626c73d.png)

  
In most cases, subflows should have a single input and output that are
represented as special nodes in the subflow editor as shown in
<span style="background: #c0c0c0">Figure 21</span>.

**Figure <span id="Figure-21" style="background: #c0c0c0">21</span>.
Subflow Example**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_5af439d4265c1240.png)

### Designing a Subflow

To design a subflow:

1.  Connect nodes starting from the input.

2.  When the flow is complete, connect the last node to the output.

**NOTE: **Subflows should not contain **service entrypoint** or
**service endpoint** nodes because the subflow does not represent a ViNO
service, but rather a small unit of work that is intended to be included
in other services.

## Working with Messages

A flow works by passing messages between nodes. The messages are simple
JavaScript objects that can have a set of properties. Messages usually
have a **payload** property, which is the default property (or object)
that most nodes work with. Messages also include an identifier property
called **\_msgid** that traces a node's progress through a flow. The
value of a message property can be a valid JavaScript type, such as:

  - Boolean

  - Number

  - String

  - Array

  - Object

  - Null

### Changing Message Properties

A common task in a flow is to modify the properties of a message as it
passes between nodes. For example, the result of an HTTP request may be
an object with many properties, of which only some are needed. There are
two main nodes for modifying a message:

  - **function** node – Enables you to run JavaScript code against the
    message. This gives you complete flexibility in what is done with
    the message, but does require familiarity with JavaScript and is
    unnecessary for many simple cases. See
    <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    the Function Node</span></span>.

  - **change** node – Provides functionality without the need to write
    JavaScript code. This node modifies message properties and also
    accesses flow- and global-context. See
    <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    the Change Node</span></span>.

### Using the Service Status Node

The
<span style="text-decoration: none"><span style="background: #c0c0c0">service
status</span> </span>node enables you to inject custom status messages
at any stage into a service. The message displayed is provided in the
node configuration and can be templated using the Mustache syntax to
display input parameters defined on the node by referencing them with
{{parameter\_key}}. This feature is useful for displaying status for
non-ViNO nodes that do not write status messages.

## Working with the Sidebar

The sidebar contains icons that provide tools within the Service
Manager:

  - ![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_664dd68233159782.png)
    Node information – View information about nodes.

  - ![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_ce4218e56113a813.png)
    Project history – Displays changes to local files and changes to
    commit.

  - ![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_92937961df0c965b.png)
    Debug messages – View messages passed to debug nodes.

  - ![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_c3af7c8d2aeb64ee.png)
    Informational dropdown that lists the display options.

  
  

<span style="background: #c0c0c0">Figure 22</span> shows the display
screen for Node Information.

**Figure <span id="Figure-22" style="background: #c0c0c0">22</span>.
Service Manager Sidebar**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_a7e212038e37ff9c.png)

  
  

To open a display, click an icon in the header of the sidebar or, select
it from the **Informational** drop-down
![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_bf88d74fcadfd287.png)
.

## Using Parameters

One of the main features of ViNO is how it handles the parameters used
to drive service activations. There are two types of parameters that
apply to ViNO nodes:

  - **Input parameters** – Control how each step activates a service.

  - **Output parameters** – Hold information that is output by a step in
    a flow that may be useful later in the service.

Parameters are unique to the
<span style="text-decoration: none"><span style="background: #c0c0c0">custom
nodes provided with ViNO</span></span>. However, you can use these
parameters to manipulate other Node-RED nodes using the **parameter
wrapper** node with the **Mode** set to **Parameter
Injection/Extraction** to inject and extract data into a Node-RED
message.

Refer to the following sections for information on using parameters.

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Configuring
    Parameters on Nodes</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Editing
    Parameters</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Parameter Mapping</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Parameter Mappings and Conditionals</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Parameter Wrapper Injection and Extraction</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Parameter Combiner Modes</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Passing
    Parameters Between a Parent Flow and Subflow</span></span>

### Configuring Parameters on Nodes

Parameters are configured on a node in the **Property Edit** window.
Double-click a node to open the **Property Edit** window specific to
that node. <span style="background: #c0c0c0">Figure 23</span> shows an
example of the **Property Edit** window for the **loop start** node.
Depending on the node selected, additional fields may be displayed.

**Figure <span id="Figure-23" style="background: #c0c0c0">23</span>.
Property Edit Window**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_76caa69ffd1de32c.png)  
![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_d15252d562dd66fe.png)  
  
  

<span id="Table-12" style="background: #c0c0c0">Table 12</span>
describes the fields, buttons, sections, and columns in the **Property
Edit** window.

**Table <span style="background: #c0c0c0">12</span>. Property Edit
Window**

<table>
<thead>
<tr class="header">
<th><p>Component</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Top navigation bar</p></td>
<td><ul>
<li><p><strong>Delete</strong> – Deletes the node.</p></li>
<li><p><strong>Cancel</strong> – Cancels changes you made in Edit mode.</p></li>
<li><p><strong>Done</strong> – Saves changes and closes the Edit Parameters window.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Name</strong> field</p></td>
<td><p>Displays the name of the node in the flow.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Description</strong> field</p></td>
<td><p>Displays a description of the node (if one was entered when the parameter was added).</p></td>
</tr>
<tr class="even">
<td><p><strong>Command</strong> field</p></td>
<td><p>Determines the action the node takes for a step.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Status Message Options</strong> button</p></td>
<td><p>This button enables you to limit the type of messages per node that are displayed at activation. Select <strong>Always</strong>, <strong>Debug mode only</strong>, or <strong>Never</strong> from each drop-down as needed:</p>
<ul>
<li><p><strong>Display Node Starting Messages</strong></p></li>
<li><p><strong>Display Node Completed Messages</strong></p></li>
<li><p><strong>Display Retry Messages</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Input Parameters</strong> section</p></td>
<td><p>Displays the parameters configured for the node. Provides buttons to add, edit, or remove parameters as well as restore defaults and unset parameters. These functions are listed in the following rows.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Add Parameter</strong> button</p></td>
<td><p>Opens the <strong>Edit Input Parameter</strong> window enabling you to add a new parameter. Depending on the option selected in the <strong>Type</strong> and <strong>Parameter Source</strong> fields, other fields may be displayed.</p>
<p>The following fields apply to all nodes:</p>
<ul>
<li><p><strong>Name</strong> – Enter a descriptive name for the parameters.</p></li>
<li><p><strong>Key</strong> – This field auto-populates as you type in the <strong>Name</strong> field.</p></li>
<li><p><strong>Description</strong> – Enter a description of the parameter.</p></li>
<li><p><strong>Type</strong> – Select a type from the drop-down.</p></li>
<li><p><strong>Parameter Source</strong> – Select a source from the drop-down:</p></li>
</ul>
<ul>
<li><p><strong>Node Configuration</strong> – Requires you to add a value in the <strong>Value</strong> field.</p></li>
<li><p><strong>Message</strong> – Requires you to add a name in the <strong>Message Property Name</strong> field. Enables you to get a value from the Node-RED message object and use it as the parameter source.</p></li>
<li><p><strong>File Reference</strong> – Select a file from the <strong>Project Files</strong> drop-down or upload a file. Enables you to use a value in a file as the parameter source.</p></li>
<li><p><strong>Constants</strong> – Enables you to use a constants file as the parameter source. Requires you to enter a path in the <strong>Constants Path</strong> field using the value in the <strong>Name</strong> fields for the settings. For example, <strong>/categoryName/groupName/scalarName</strong>. Several constants are<br />
pre-populated as you type.</p></li>
<li><p><strong>Mapped from another Node (ViNO Service Only)</strong> – Enables you to select the node that has the parameter you want to map from (in the <strong>Mapped From Node</strong> field). You must then select the key you want to map from in the <strong>Mapped from Key</strong> field.</p></li>
</ul>
<ul>
<li><p><strong>Display Order Index</strong> – Use the arrow buttons to determine the order in which parameters are displayed. The lower the number, the higher the entry appears in the display.</p></li>
<li><p><strong>Optional</strong> – Select this button to make the parameter optional. If <strong>Optional</strong> is not selected, the parameter is required by default to activate the service.</p></li>
<li><p><strong>Final</strong> – Select this button to disable the ability to change the parameter at activation. Parameters that have this option selected are not displayed in on the <strong>Activation</strong> screen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Edit Parameter</strong> button</p></td>
<td><p>Opens the <strong>Edit Input Parameter</strong> window enabling you to edit parameters for a specific node. Highlight a node entry and then click Edit Parameter (or double-click a parameter). Includes similar fields as the <span style="text-decoration: none"><span style="background: #c0c0c0">Add Parameter button</span></span>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Remove Parameter</strong> button</p></td>
<td><p>Enables you to remove user-added parameters. You cannot remove built-in parameters.</p></td>
</tr>
<tr class="even">
<td><p><strong>Restore Defaults</strong> button</p></td>
<td><p>Restores the default value (as displayed in the <strong>Parameter Value</strong> column) for the selected parameter.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Unset Parameter</strong> button</p></td>
<td><p>Clears the value (as displayed in the <strong>Parameter Value</strong> column) for the selected parameter.</p></td>
</tr>
<tr class="even">
<td><p><strong>Parameter Name</strong> column</p></td>
<td><p>Displays the name of the input parameter.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Parameter Description</strong> column</p></td>
<td><p>Displays a description of the input parameter if one was entered in the <span style="text-decoration: none"><span style="background: #c0c0c0">Description</span></span> field.</p></td>
</tr>
<tr class="even">
<td><p><strong>Parameter Key</strong> column</p></td>
<td><p>Displays the input parameter key for the node.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Parameter Value</strong> column</p></td>
<td><p>Displays the input parameter value if one has been configured on the node or displays the source for the value.</p></td>
</tr>
<tr class="even">
<td><p><strong>Display Order</strong> column</p></td>
<td><p>Displays a parameter in a specific order if the <span style="text-decoration: none"><span style="background: #c0c0c0">Display Order Index</span> </span>field is set.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Output Parameters</strong> section</p></td>
<td><p>Displays the parameters that are configured to contain the output of the node. Provides buttons to add, edit, or remove output parameters as well as restore defaults. These functions are listed in the following rows.</p></td>
</tr>
<tr class="even">
<td><p><strong>Add Parameter</strong> button</p></td>
<td><p>Open the Edit Output Parameter window enabling you to add an attribute to the Node-RED message object that contains the value of the output parameter.</p>
<ul>
<li><p><strong>Name</strong> – Enter a descriptive name for the parameters.</p></li>
<li><p><strong>Key</strong> – This field auto-populates as you type in the <strong>Name</strong> field.</p></li>
<li><p><strong>Description</strong> – Enter a description of the parameter.</p></li>
<li><p><strong>Type</strong> – Select a type from the drop-down.</p></li>
<li><p><strong>Extraction Method</strong> – Select a method from the drop-down to determine how data is extracted from the output of a node. If you select REGEX, XPATH, or JSONPath, you must provide a valid rule in the <strong>Format</strong> field.</p></li>
<li><p><strong>Format</strong> – Enter a valid rule if you selected REGEX, XPATH, or JSONPath as an extraction method.</p></li>
<li><p><strong>Inject into msg as</strong> – Enables you to inject the ViNO output parameter into the Node-RED msg object using the identifier entered in this field.</p></li>
<li><p><strong>Private</strong> – This checkbox prevents other nodes from being able to use parameter mapping to reference this output parameter.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Edit Parameter</strong> button</p></td>
<td><p>Opens the <strong>Edit Output Parameter</strong> window enabling you to edit parameters for a specific node. Highlight a node entry, then click Edit Parameter. Or, double-click a parameter. Includes the same fields as the <span style="text-decoration: none"><span style="background: #c0c0c0">Add Parameter</span></span> button.</p></td>
</tr>
<tr class="even">
<td><p><strong>Remove Parameter</strong> button</p></td>
<td><p>Enables you to remove user-added parameters. You cannot remove built-in parameters.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Restore Defaults</strong> button</p></td>
<td><p>Restores the default value (as displayed in the <strong>Parameter Value</strong> column) for the selected parameter.</p></td>
</tr>
<tr class="even">
<td><p><strong>Parameter Name</strong> column</p></td>
<td><p>Displays the name of the output parameter.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Parameter Description</strong> column</p></td>
<td><p>Displays a description of the output parameter if one was entered in the <span style="text-decoration: none"><span style="background: #c0c0c0">Description</span></span> field.</p></td>
</tr>
<tr class="even">
<td><p><strong>Parameter Key</strong> column</p></td>
<td><p>Displays the output parameter key for the node.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Parameter Format</strong> column</p></td>
<td><p>Displays the rule entered in the <span style="text-decoration: none"><span style="background: #c0c0c0">Format</span></span> field. This value displays when REGEX, XPATH, or JSONPath was selected as an extraction <span style="text-decoration: none"><span style="background: #c0c0c0">method</span></span>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Extraction Method</strong> column</p></td>
<td><p>Displays the method as set in the <span style="text-decoration: none"><span style="background: #c0c0c0">Extraction Method</span></span> field.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Inject into msg as</strong> column</p></td>
<td><p>Displays the identifier entered in the <span style="text-decoration: none"><span style="background: #c0c0c0">Inject into msg as</span></span> <strong></strong> field.</p></td>
</tr>
</tbody>
</table>

### Editing Parameters

To edit a parameter, select it from the **Input Parameters** section of
the **<span style="background: #c0c0c0">Property Edit </span>**window,
and then click **Edit Parameter** or double-click the parameter name.
<span style="background: #c0c0c0">Figure 24</span> shows an example of
the **Edit Input Parameter** window.

**Figure <span id="Figure-24" style="background: #c0c0c0">24</span>.
Edit Input Parameter Window**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_8258dd88b14fef6d.png)

  
  

The **Edit Input Parameter** window includes fields and checkboxes that
control the behavior of parameters and the **Value** field in which a
fixed value can be set. Because this parameter is built into the action,
some fields and options are disabled. When the parameter is configured
to come from constants or is mapped from another node, additional fields
appear that enable you to configure which constant to lookup or to which
node and parameter to map.

  - The **Final** checkbox controls whether the value can be overridden
    at activation time. When mapping from another node, the **Final**
    checkbox cannot be selected.

  - The **Optional** checkbox controls whether the service can activate
    with or without that parameter.

### Using Parameter Mapping

Parameter mapping enables you to reference a parameter value from a node
that had been activated previously. For example, you may reference a VM
ID in a deactivation step in order to delete the VM. When mapping to
previous nodes, map to output parameters (not input parameters).

**Caution**: Do not use the **Import** or **Export** options
(<span style="background: #c0c0c0">Menu </span>icon drop-down) to share
or save a project. These functions lose parameter mappings.

### Using Parameter Mappings and Conditionals

ViNO conditional nodes (conditional start and conditional end) present a
unique challenge when it comes to parameter mapping. This is because the
conditional statement is not evaluated until activation time and its
input values may be based on previous steps or user input. The result of
the evaluation cannot be known ahead of time. Therefore, there is no
guarantee when designing a service that the steps in one particular
branch will be executed. For that reason, nodes outside of a particular
conditional branch are not permitted to map to parameters on nodes
within a conditional branch. However, you may need to use output
parameters from steps within a conditional later in the service flow
after the conditional branch has completed.

To accomplish this, configure the
<span style="text-decoration: none"><span style="background: #c0c0c0">conditional
end</span></span> node with a unique type of output parameter that
handles this situation in a safe manner. Output parameters in the
**conditional end** node are configured to map to parameters in both the
true and false branches. This functionality imposes the limitation that
both branches must contain a parameter that logically makes sense to
expose in both the true and false scenarios.

### Using Parameter Wrapper Injection and Extraction

The
<span style="text-decoration: none"><span style="background: #c0c0c0">parameter
wrapper</span></span> node has several different purposes. The **Mode**
setting controls the behavior of the node.

When a **parameter wrapper** node has the mode set to **Parameter
Injection/Extraction**, the node injects input parameters into the
Node-RED message object so that the parameters can be accessed with
**msg.parameter\_key**. This node also inspects output parameters
defined on it and tries to extract the parameters from the Node-RED
message object. This functionality is necessary to facilitate the use of
non-ViNO nodes in a service flow. The **parameter wrapper** node can
also be used to pass parameters into subflows.

### Using Parameter Combiner Modes

The **Parameter Combiner** modes (**Mode** drop-down in the **Property
Edit** window) provide a simple way to transform individual scalar
parameters in to a single list type parameter. Input parameters added in
this mode are included in the **Combined Output List** parameter. The
**Parameter Combiner** modes available in the **Mode** drop-down
include:

  - **Parameter Combiner (String)**

  - **Parameter Combiner (Number)**

  - **Parameter Combiner (Boolean)**

<span style="background: #c0c0c0">Figure 25</span> shows the **Mode**
field in the **Property Edit** window.

**Figure <span id="Figure-25" style="background: #c0c0c0">25</span>.
Mode Field in Property Edit Window**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_6cb5557957b059b9.png)

### Passing Parameters Between a Parent Flow and Subflow

Parameters can be passed between a subflow and the
<span style="text-decoration: none"><span style="background: #c0c0c0">parent
flow</span> </span>that is<span style="text-decoration: none">
</span>using it. When accessing the output parameters of nodes within
the subflow from the parent flow, ViNO combines them and presents them
as output parameters of the subflow node within the parent flow.
However, passing parameters into the subflow is complex because nodes
within a subflow cannot use the ViNO parameter mapping functionality to
directly map to any parameters in a parent flow. This is because
subflows can be used in different flows. To work around this, use the
<span style="text-decoration: none"><span style="background: #c0c0c0">parameter
wrapper</span></span> **** node with the **Mode** set to **Parameter
Injection/Extraction**.

At the start of the subflow, add a **parameter wrapper** node and define
output parameters to contain any values you want to pass into the
subflow from the parent flow.

Nodes within the subflow can now map to those output parameters as
needed. To pass those parameters into the subflow:

1.  Add another **parameter wrapper** node immediately in the parent
    flow *before* the subflow.

2.  Define input parameters on the **parameter wrapper** node that
    exactly match the parameter keys from the output parameters created
    within the subflow.

When the service is activated, the two input parameters in the parent
flow are put into the message object, which gets passed into the subflow
where they are immediately extracted into two corresponding output
parameters. When a flow uses a subflow that requires certain parameters
to be passed in and the parent flow fails to do so, the subflow triggers
an activation failure due to missing input.

**NOTE: **When the subflow requires the parameters for use in built-in
nodes, you can omit the **parameter wrapper** node at the start of the
subflow. This is because the parent flow has already placed the
parameters on to the message object so that they can be directly
accessed by built-in nodes as is.

<span style="background: #c0c0c0">Figure 26</span> shows an example of
the Edit Property window for a parameter wrapper node.

**Figure <span id="Figure-26" style="background: #c0c0c0">26</span>.
Using a Parameter Wrapper Node**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_4b8b3aa9e2d8a67f.png)  
![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_e10227d7269deaaa.png)

  
  

## Using Loops

It may be necessary to repeat a step or a group of steps in a service
multiple times. The number of times to repeat these steps may be
variable or the input for each iteration may need to vary. The
<span style="background: #c0c0c0">loop start</span> and the
<span style="background: #c0c0c0">loop end</span> nodes provide two ways
to perform a set of actions repeatedly:

  - A basic loop that repeats a fixed number of times

  - A **for each** loop that iterates over a list and exposes a single
    element from that list upon each iteration.

Refer to the following sections for information on using loops:

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Basic Loops</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Considerations
    for Each Loop</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Input Parameters in a Loop Step</span></span>

  - <span style="text-decoration: none"><span style="background: #c0c0c0">Using
    Parameter Mapping and Loops</span></span>

### Using Basic Loops

A basic loop begins with a <span style="background: #c0c0c0">loop
start</span> node that contains a single input parameter (Iterations)
that controls the number of times the loop is to repeat. The
<span style="text-decoration: none"><span style="background: #c0c0c0">parameter
source</span></span> can be configured using the same sources available
to other input parameters. The **loop start** node contains a single
output parameter that always contains the current iteration number of
the loop starting from 0. A node within a loop can map any of its
parameters to the Iterations input parameter in the **loop start** node.

The **loop start** node has two output ports:

  - The top output connects to the start of the steps that are included
    in the loop (the loop body).

  - The bottom output connects to the next step to take after the loop
    has run to completion.

As shown in <span style="background: #c0c0c0">Figure 27</span>, at the
end of the loop body, the last node must connect to a **loop end** node
that must connect back to the input of the **loop start** node.

**Figure <span id="Figure-27" style="background: #c0c0c0">27</span>.
Example of a Basic Loop**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_3d8ee1f6b912828b.png)

### Considerations for Each Loop

In addition to the basic loop mode, ViNO provides another looping mode
that resembles the **for each** construct of many programming languages.
This loop mode operates identically to the basic loop mode, but rather
than taking a number that controls the number of iterations in the
**start** node, the loop takes a list type input parameter called
**Input List**. The type of this list is determined by which variation
of the **for each** mode is selected (String, Number, or Boolean). There
is also a single output parameter (**Current Value**) that contains the
value for the current iteration of the loop.

<span style="background: #c0c0c0">Figure 28</span> shows the **loop
start** node with the **Input List** parameter and the mode set to **For
Each Loop** with a string input list. The input list contains three
values (VM1, VM2, and VM3), indicating that the loop is to run a total
of three times. The **Current Value** output parameter has its value set
to VM1 on the first iteration, VM2 on the second iteration, and VM3 on
the third iteration.

**Figure <span id="Figure-28" style="background: #c0c0c0">28</span>.
Using Input List in a Loop**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_45231b7a1d494dd4.png)

<span style="background: #c0c0c0">Figure 29</span> shows the Create VM
node with the Virtual Machine Name input parameter value mapped to the
**Current Value** output from the preceding **loop** **start** node.
Because that parameter changes with each iteration, the end result of
this loop would be three VMs with the names VM1, VM2, and VM3.

**Figure <span id="Figure-29" style="background: #c0c0c0">29</span>.
Loop Start Node Example**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_b0cafe265df1b5d2.png)

### Using Input Parameters in a Loop Step

To provide flexibility, the input parameters of a node have a unique
behavior when the parameters are located inside the body of a loop. When
a parameter is configured in a node and not overridden, it uses that
fixed value for every iteration of the loop. However, if the input
parameter is provided at activation time, its type is converted into a
corresponding list type (for example, a string parameter becomes a
**stringList parameter**) and the step uses the next value available in
that list upon each iteration.

For example, if the “Create VM” step was placed inside a loop, the **VM
Name** input parameter would be converted to a **stringList**. The loop
could then be configured to run for three iterations and the **VM Name**
parameter could be given a list of three different names. This would
result in the creation of three virtual machines, each with one of the
names provided in the **VM Name** input parameter list. The loop would
also wrap around while iterating through input lists, if necessary.
Therefore, if a loop runs six times, but a particular input list only
contains two values, the loop alternates between those two values for
that particular parameter.

### Using Parameter Mapping and Loops

For nodes that map to parameters of nodes within the same loop,
<span style="text-decoration: none"><span style="background: #c0c0c0">parameter
mapping</span></span> works as expected and the mapping copies the value
from the node activated within the current iteration. However, if a
parameter in a node outside of the loop maps to a parameter in a node
within the loop, it always receives the value used or created on the
last iteration of the loop.

## Using Parallel Execution

Node-RED and ViNO natively support executing independent steps in
parallel. Each node output can have multiple connections to subsequent
nodes. To create a parallel branch, create links from one node output to
two or more nodes.

**NOTE: **Because nodes within parallel branches cannot map to nodes in
other branches, parallel logic can only be employed when a series of
actions are truly independent.

As shown in <span style="background: #c0c0c0">Figure 30</span>, after
the network is created, the service splits into three branches and
begins creating three VMs in parallel.

**Figure <span id="Figure-30" style="background: #c0c0c0">30</span>.
Example of Creating a Parallel Branch**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_a9f2a96d5bb5692a.png)

### Joining Parallel Branches

Before a service completes, it must join the parallel branches together
at some point. This is a point that halts execution of the service until
all branches are finished completely. The last node of each branch must
be connected to a single **join** node as shown in
<span style="background: #c0c0c0">Figure 31</span>.

**Figure <span id="Figure-31" style="background: #c0c0c0">31</span>.
Example of Joining Parallel Branches**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_b9ce6a0299508c2a.png)

The **join** node must then be configured to expect message from the
number of branches that were created. To accomplish this:

1.  Open the **Property Edit** window for the **join** node. See
    <span style="background: #c0c0c0">Figure 32</span>.

2.  Select **manual** mode.

3.  (Optional) Select values for the following fields:

<!-- end list -->

  - **to create**

  - **joined using**

  - **After a timeout following the first message**

<!-- end list -->

4.  Enter the number of branches being joined in the field **After a
    number of message parts**.

5.  Click Done.

After the branches have been joined, the service can continue as normal
and all nodes within the branches can be referenced using
<span style="text-decoration: none"><span style="background: #c0c0c0">parameter
mapping</span></span>.

**NOTE: **Failure to configure the **join** node correctly results in
undefined behavior.

**Figure <span id="Figure-32" style="background: #c0c0c0">32</span>.
Example of Join Node Properties**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_de9a8efdc303a13a.png)  
  
  

  
  

# Creating a Service Deactivation Flow

To create a service deactivation flow, use the
<span style="text-decoration: none"><span style="background: #c0c0c0">service
entrypoint</span></span> node. This node has two outputs available:

  - Top output – Used for the service activation flow.

  - Bottom output – Meant to be connected to a corresponding flow that
    would deactivate an instance of the service.

**NOTE: **A service flow must have a deactivation path defined in order
for the service to be deactivated.

A service deactivation flow works similarly to how the activation flows
work with several key differences:

  - At the end of a deactivation flow, the last node must be connected
    to a
    <span style="text-decoration: none"><span style="background: #c0c0c0">deactivation
    endpoint</span></span> node rather than a
    <span style="text-decoration: none"><span style="background: #c0c0c0">service
    endpoint</span></span> node.

  - Nodes within the deactivation flow can map to parameters from a node
    in the activation flow. This enables the deactivation flow to access
    the input and output information that was used or created during a
    particular activation as part of the deactivation logic. For
    example, if a VM was created in an activation flow, the flow would
    need the VM identifier output as part of that step in the
    deactivation flow to delete the correct VM.

  - The deactivation flow ignores errors encountered during deactivation
    and continues deactivating. This is to facilitate easier rollback
    logic and ensure that ViNO tears down as much of the service as
    possible, even if some resources are missing or have been modified
    since the service activation. Errors in the deactivation flow are
    still reported in status messages.

<span style="background: #c0c0c0">Figure 33</span> shows an example of a
simple service with a corresponding deactivation flow.

**Figure <span id="Figure-33" style="background: #c0c0c0">33</span>.
Service with Corresponding Deactivation Flow**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_9e20dd9ea1b5ebe7.png)

  
  

When a deactivation is called on an instance of a service, the inputs
and outputs from the activation are retrieved and available for use.
<span style="background: #c0c0c0">Figure 34</span> shows a deactivation
flow that maps to the VM ID output parameter from the activation flow,
which deletes the VM associated with that particular activation.

**Figure <span id="Figure-34" style="background: #c0c0c0">34</span>.
Deactivation Flow Example**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_4e075d0f3841c15c.png)

  
  

# Error Handling

Due to the complexity of certain service activation flows, errors may
occur. For example, if there are invalid or missing inputs or
unreachable systems, service activations will fail to complete
successfully. It is important to handle cases where failure is a
possibility. Node-RED and ViNO include the ability to automatically
handle errors using the:

  - **catch** node

  - **throw** node

## Using the Catch Node

If a node encounters a problem, it triggers an error and stops passing
messages to subsequent nodes. The Node-RED **catch** node (located under
the
<span style="text-decoration: none"><span style="background: #c0c0c0">input</span></span>
category) can intercept these errors and start executing a flow from an
entirely independent location. You can configure the **catch** node to
either catch errors from anywhere on the current flow or to only catch
errors from specified nodes. This functionality provides flexibility for
handling errors.

However, it is necessary to communicate to ViNO in the case of Node-RED
errors, which is the function of the
<span style="text-decoration: none"><span style="background: #c0c0c0">service
failure</span></span> node. When a **service failure** node executes,
ViNO records that the service activation was a failure and reports this
in a status message. When a service encounters an error that is not
directed to a **service failure** node, ViNO does not record the
activation attempt. Therefore, services should have a minimum of one
**catch** node connected to a **service failure** node. Both nodes can
be placed anywhere on the same tab as the activation flow.

The **catch** node can also be configured to catch errors only from
specified nodes. This can be useful in defining rollback logic for a
service. See
<span style="text-decoration: none"><span style="background: #c0c0c0">Adding
Rollback Capability</span></span>.

## Using the Throw Node

The ViNO
<span style="text-decoration: none"><span style="background: #c0c0c0">throw</span></span>
node simply throws an error upon reaching a node. This node functions as
a valid end (such as the **service endpoint** and the **deactivation
endpoint** nodes) to a ViNO service, which allows the service to
complete even in the case of an error.

### Adding Rollback Capability

If a service runs into an error at some point in the activation process,
it may be necessary to clean up or revert some of the actions that
completed prior to the failure. This can be done by combining the error
handling capabilities (see
<span style="text-decoration: none"><span style="background: #c0c0c0">Error
Handling</span></span>) with the deactivation flow.

The
<span style="text-decoration: none"><span style="background: #c0c0c0">service
failure</span></span> node contains an output that may optionally be
connected to a node in the deactivation flow. If a service encounters an
error and ViNO detects that the **service failure** node is connected to
the deactivate flow, it enters rollback mode and indicates that it is
now trying to clean up the failed activation. The easiest way to
implement rollback is to:

1.  Use a single **catch** node and select **all nodes** from the
    **Catch Errors From** drop-down.

2.  Connect it to a **service failure** node.

3.  Connect **service failure** node to the first node of the deactivate
    flow.

<span style="background: #c0c0c0">Figure 35</span> shows how to
implement a rollback.

**Figure <span id="Figure-35" style="background: #c0c0c0">35</span>.
Implementing a Rollback**

![](img/Virtual%20Network%20Orchestrator%20User%20Guide_html_ce428f5b855c3e8a.png)

  
Because nodes in a deactivation flow ignore errors, a rollback always
runs to completion even if some of the actions attempting to be
deactivated were never activated.

<div title="footer">

  

</div>
