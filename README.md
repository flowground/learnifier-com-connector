# ![LOGO](logo.png) Learnifier **flow**ground Connector

## Description

A generated **flow**ground connector for the Learnifier API (version 1.1.0).

Generated from: https://api.apis.guru/v2/specs/learnifier.com/1.1.0/swagger.json<br/>
Generated at: 2019-06-06T16:12:24+03:00

## API Description



## Authorization

This API does not require authorization.

## Actions

### Lists all global course design templates

> Lists all global course design templates. Only api callers that have full access can call this method.

*Tags:* `Course Designs`

### Get Organization Unit with External Id

> Returns information about the organization unit with the specified external id.

*Tags:* `Organization Units`

#### Input Parameters
* `extid` - _required_ - The external id of the organization unit

### Gets a participation by external id

> Gets a participation by external id.

*Tags:* `Users`

#### Input Parameters
* `extid` - _required_ - The external id of the participation

### Gets Organization Unit by external id

> Gets an Organization Unit by external id

*Tags:* `Projects`

#### Input Parameters
* `extid` - _required_ - The external id of the organization unit

### Gets a user by external id

> Gets a user by external id.

*Tags:* `Users`

#### Input Parameters
* `extid` - _required_ - The external id of the user

### List Global User Groups.

> Returns a list of Global User Groups. Global User Groups are set up for the realm, and will generate groups that can be used on the client level.

*Tags:* `Global User Groups`

### List of all users in group.

> Returns a list of all members in User Groups that are based on the Global Group with this groupid.

*Tags:* `Global User Groups`

#### Input Parameters
* `groupid` - _required_ - ID of group

### Organization Units

> The orgunits endpoint returns information about the available organization units (orgunits).<br/>
> The response includes the display name, internal and external id and client number.

*Tags:* `Organization Units`

### Adds an Organization Unit

*Tags:* `Organization Units`

### Get Organization Unit

> Returns information about the specified organization unit.<br/>
> The response includes the display name, internal and external id and client number.

*Tags:* `Organization Units`

#### Input Parameters
* `orgid` - _required_ - Id of the organization unit

### Updates an Organization Unit

> Adds an Organization Unit

*Tags:* `Organization Units`

#### Input Parameters
* `orgid` - _required_

### Organization Unit Projects

> Returns the available projects for the organization unit

*Tags:* `Projects`

#### Input Parameters
* `orgid` - _required_ - Id of the organization unit

### Create project

> Creates a new project

*Tags:* `Projects`

#### Input Parameters
* `orgid` - _required_ - Id of the organization unit

### Deletes the project

> Deletes the project. The project can only be deleted if the project do not contain any participants.

*Tags:* `Projects`

#### Input Parameters
* `orgid` - _required_ - Id of the organization unit
* `projectid` - _required_ - Id of the project

### Project information

> Returns project information

*Tags:* `Projects`

#### Input Parameters
* `orgid` - _required_ - Id of the organization unit
* `projectid` - _required_ - Id of the project

### Update project information

> Updates information about a project. Values are only updated if the fields are specified in the input

*Tags:* `Projects`

#### Input Parameters
* `orgid` - _required_ - Id of the organization unit
* `projectid` - _required_ - Id of the project

### Project participants

> Returns project participants

*Tags:* `Projects`

#### Input Parameters
* `orgid` - _required_ - Id of the organization unit
* `projectid` - _required_ - Id of the project

### Add participant

> Add a user to the project. Participant information is created for the user. In the body object, only one of either email or userid must be specified. The participant needs to be activated before it the user can access it.

*Tags:* `Projects`

#### Input Parameters
* `orgid` - _required_ - Id of the organization unit
* `projectid` - _required_ - Id of the project

### Deletes a participant

> Deletes a participant. The user itself will still remain but any state related to the project will be deleted.<br/>
> It might not be possible due to constraints from the products in the project to delete the participant. However<br/>
> this can only be determined at the time of the delete. If a delete fails the participant will have their inError<br/>
> flag set.

*Tags:* `Projects`

#### Input Parameters
* `orgid` - _required_ - Id of the organization unit
* `projectid` - _required_ - Id of the project
* `participantId` - _required_ - Participant id

### Activate participant

> Activates a participant so that it can be used

*Tags:* `Projects`

#### Input Parameters
* `orgid` - _required_ - Id of the organization unit
* `projectid` - _required_ - Id of the project
* `participantId` - _required_ - Id of the participant

### Participant login link

> Returns a single sign on link for the participant. The link is only usable once and should be used directly. The link expires after a few minutes.<br/>
> <br/>
> This operation requires the *login link* permission.

*Tags:* `Projects`

#### Input Parameters
* `orgid` - _required_ - Id of the organization unit
* `projectid` - _required_ - Id of the project
* `participantId` - _required_ - Id of the participant

### Project team members

> Returns the project team members. A team member is a ....

*Tags:* `Projects`

#### Input Parameters
* `orgid` - _required_ - Id of the organization unit
* `projectid` - _required_ - Id of the project

### List User Groups.

> Returns a list of User Groups for the org unit.

*Tags:* `User Groups`

#### Input Parameters
* `orgid` - _required_ - ID of organization

### Create a User Group.

> Create a User Group.

*Tags:* `User Groups`

#### Input Parameters
* `orgid` - _required_ - ID of organization

### Get user group

> Returns single User Group.

*Tags:* `User Groups`

#### Input Parameters
* `orgid` - _required_ - ID of organization
* `groupid` - _required_ - ID of group

### List of all users in group.

> Returns a list of all members in User Groups that are based on the Global Group with this groupid.

*Tags:* `User Groups`

#### Input Parameters
* `orgid` - _required_ - ID of organization
* `groupid` - _required_ - ID of group

### Add user group member.

> Adds a user to user group.

*Tags:* `User Groups`

#### Input Parameters
* `orgid` - _required_ - ID of organization
* `groupid` - _required_ - ID of group

### Remove user group member.

> Removes a user from a user group.

*Tags:* `User Groups`

#### Input Parameters
* `orgid` - _required_ - ID of organization
* `groupid` - _required_ - ID of group
* `uuid` - _required_ - UUID of user to remove from group.

### Lists all users

> Lists all users. Only api callers that have full access can call this method.

*Tags:* `Users`

#### Input Parameters
* `limit` - _optional_ - The maximum number of users to return
* `offset` - _optional_ - The offset to start listing users from

### Adds a user

> Adds a user. No two users can have the same email address. Email is saved WITH case but compared regardless of case. Email can be changed for a user assuming it doesn't cause a conflict.

*Tags:* `Users`

### User information

> Returns information about a user

*Tags:* `Users`

#### Input Parameters
* `userid` - _required_ - A user id

### Updates user information

> Updates a user. All values that have a key defined in the input will be set. So if a value should not be updated omit it totally from the input, otherwise it will be unset.

*Tags:* `Users`

#### Input Parameters
* `userid` - _required_ - The user id

### User profile picture

> Returns a thumbnail picture of the user. This can either be a selected picture or an auto generated image. This method doesn't require a full sign in. The api key is sufficient.<br/>
> The image is square and is likely, but not necessary, to be in 128x128 PNG format. However the format will always be either PNG, JPEG or GIF.

*Tags:* `Users`

#### Input Parameters
* `userid` - _required_ - The user id
* `APIKEY` - _required_

### Returns information about the projects the user is a participant in.

> Returns information about the projects the user is a participant in. Only the projects that the current token have access to will be listed.

*Tags:* `Users`

#### Input Parameters
* `userid` - _required_ - A user id

## License

**flow**ground :- Telekom iPaaS / learnifier-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
