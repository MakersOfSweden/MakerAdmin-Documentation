# Permissions
MakerAdmin have a very flexible permission system.

## Users
To give a user permission to something the user should be added to an role.

Example:
  - The user `Master Ninja` have the role `Administrator`.
  - The user `John Doe` have the role `Key Handout`.

## Groups
A group is a way to cetegorize members. A member could be added to one or more groups.

Example:
  - All new members are automaticcally added to the group `New members`.
  - All members without a key are added to the group `Key handout`.
  - All members that want to recieve the newsletter E-mail is added to a group `Newsletter`.

## Roles
A role is used to collect a bunch of permissions and give them to a user.

Example:
  - The role `Adminstrator` gives the user access to everything without any limitations-
  - The role `Key handout` gives the user access to list all members in the group `Key handout`.

## Permissions
Most of the modules in the systems registers permissions that could be used in a role. A permission is always attached to a group.

### Api Gateway
  - api register - Register a new service to the API
  - api exec - Execute commands in a registered service

### Membership module
  - member create - Create a new member
  - member delete - Delete an existing member
  - member edit - Edit all details of a member (Address, phone number, etc)
  - member view - View all details of a member (Address, phone number, etc)
  - group create   Create a new group
  - group delete - Delete an existing member
  - group edit - Edit all details of a group (Title, description, etc)
  - group view - View all details of a group (Title, description, etc)
  - group addmember - Add a member to a group
  - group removemember - Remove a member from a group

### Economy module
  - ***Todo***

### Invoice module
  - ***Todo***

### Sales module
  - ***Todo***

### Tictail module
  - ***Todo***

Example
  - For the role `Administrator` the permission `api register` is assigned to the group `root`. This means that all users with the role `administrator` is allowed to register new services in the group `root` or one below, which basically is all groups in the system.