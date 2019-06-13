
---
title: "jwt.proto"
weight: 5
---

<!-- Code generated by solo-kit. DO NOT EDIT. -->


### Package: `jwt.plugins.gloo.solo.io` 
#### Types:


- [VhostExtension](#vhostextension)
- [RemoteJwks](#remotejwks)
- [LocalJwks](#localjwks)
- [Jwks](#jwks)
- [RouteExtension](#routeextension)
  



##### Source File: [github.com/solo-io/solo-projects/projects/gloo/api/v1/plugins/jwt/jwt.proto](https://github.com/solo-io/solo-projects/blob/master/projects/gloo/api/v1/plugins/jwt/jwt.proto)





---
### VhostExtension



```yaml
"jwks": .jwt.plugins.gloo.solo.io.VhostExtension.Jwks
"audiences": []string
"issuer": string

```

| Field | Type | Description | Default |
| ----- | ---- | ----------- |----------- | 
| `jwks` | [.jwt.plugins.gloo.solo.io.VhostExtension.Jwks](../jwt.proto.sk#jwks) | The source for the keys to validate JWTs. |  |
| `audiences` | `[]string` | An incoming JWT must have an 'aud' claim and it must be in this list. |  |
| `issuer` | `string` | Issuer of the JWT. the 'iss' claim of the JWT must match this. |  |




---
### RemoteJwks



```yaml
"url": string
"upstreamRef": .core.solo.io.ResourceRef

```

| Field | Type | Description | Default |
| ----- | ---- | ----------- |----------- | 
| `url` | `string` | The url used when accessing the upstream for Json Web Key Set. This is used to set the host and path in the request |  |
| `upstreamRef` | [.core.solo.io.ResourceRef](../../../../../../../../solo-kit/api/v1/ref.proto.sk#resourceref) | The Upstream representing the Json Web Key Set server |  |




---
### LocalJwks



```yaml
"key": string

```

| Field | Type | Description | Default |
| ----- | ---- | ----------- |----------- | 
| `key` | `string` | Inline key. this can be json web key, key-set or PEM format. |  |




---
### Jwks



```yaml
"remote": .jwt.plugins.gloo.solo.io.VhostExtension.RemoteJwks
"local": .jwt.plugins.gloo.solo.io.VhostExtension.LocalJwks

```

| Field | Type | Description | Default |
| ----- | ---- | ----------- |----------- | 
| `remote` | [.jwt.plugins.gloo.solo.io.VhostExtension.RemoteJwks](../jwt.proto.sk#remotejwks) | Use a remote JWKS server |  |
| `local` | [.jwt.plugins.gloo.solo.io.VhostExtension.LocalJwks](../jwt.proto.sk#localjwks) | Use an inline JWKS |  |




---
### RouteExtension



```yaml
"disable": bool

```

| Field | Type | Description | Default |
| ----- | ---- | ----------- |----------- | 
| `disable` | `bool` | Disable JWT checks on this route. |  |





<!-- Start of HubSpot Embed Code -->
<script type="text/javascript" id="hs-script-loader" async defer src="//js.hs-scripts.com/5130874.js"></script>
<!-- End of HubSpot Embed Code -->