---
type: added
---
`POST /api/v1/applications/{uuid}/destinations/{destination_uuid}/deploy` endpoint that deploys an application to one destination without a redeploy of its other servers

- The endpoint returns `409` when a deployment of the application is already queued or in progress on the server of the destination
- The optional `commit` deploys a tag from the rollback images list or the commit of a successful production deployment to that destination only, as a rollback
