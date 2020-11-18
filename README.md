# Release Creator

This is a simple webapp which will create a release based on the label of `Release: Major|Minor|Patch` on the merged pull request

## Configuration

### Environment Variables

This app uses the following environments variables:

| Name | Required | Description |
| ---| --- | ---|
| GITHUB_TOKEN| Yes| Token to access the github api, create the release and update the changelog on master |
| SECRET_TOKEN | Yes| If supplied it will do a HMAC check against the incomming request |

### Webhook

To configure the webhook you will want to do the following:

```none
URL: <https://example.com/handler>
Events:
  Let me select:
    Pull Requests (Only)
```

If you set a HMAC secret ensure that `SECRET_TOKEN` is set to the same secret value

## Docker images

Docker images are supplied under Xorima on docker hub, <https://hub.docker.com/r/xorima/ReleaseCreator/>
