swagger: "2.0"
x-collection-name: Mattermost
x-complete: 1
info:
  title: Mattermost
  version: 1.0.0
host: your-mattermost-url.com
basePath: /api/v4
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{user_id}:
    delete:
      summary: Deactivate a user account.
      description: |-
        Deactivates the user by archiving its user object.
        ##### Permissions
        Must be logged in as the user being deactivated or have the `edit_other_users` permission.
      operationId: deactivates-the-user-by-archiving-its-user-object-permissionsmust-be-logged-in-as-the-user-being-dea
      x-api-path-slug: usersuser-id-delete
      parameters:
      - in: path
        name: user_id
        description: User GUID
      responses:
        200:
          description: OK
      tags:
      - Deactivate
      - User
      - Account.
  /plugins/{plugin_id}/deactivate:
    post:
      summary: Deactivate plugin
      description: |-
        Deactivate a previously activated plugin. Plugins must be enabled in the server's config settings.

        ##### Permissions
        Must have `manage_system` permission.

        __Minimum server version__: 4.4
      operationId: deactivate-a-previously-activated-plugin-plugins-must-be-enabled-in-the-servers-config-settings-perm
      x-api-path-slug: pluginsplugin-iddeactivate-post
      parameters:
      - in: path
        name: plugin_id
      responses:
        200:
          description: OK
      tags:
      - Deactivate
      - Plugin