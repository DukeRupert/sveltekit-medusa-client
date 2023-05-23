# Change Log

## 1.11.0

### Patch Changes

- fix: getProduct() will return null and not throw an error if product not found
- feat: add ability to pass a second 'options' argument to the contructor.  If present, this argument must be an object.  For now, the only handled property options is 'headers', which can be an object of custom headers to be sent with each fetch request to the Medusa server.  These headers will be in addition to, and will not replace, the session cookie and content type headers the client already sends.  For example, if your Medusa server sits behind a cloudflared tunnel with access key security, you can now pass an additional header with the access key through the client.