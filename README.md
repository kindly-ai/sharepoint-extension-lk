## kindly-chat-extension

This is an example Sharepoint extension to load Kindly.

The approach is based on [a migration path for legacy sharepoint scripts](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/extensions/guidance/migrate-from-usercustomactions-to-spfx-extensions).

Use can use this code as a basis for your own Sharepoint installation. Before deploying you need to your bot key in `src/extensions/kindlyChatExtension/KindlyChatExtensionApplicationCustomizer.ts`. This is the same bot you find on app.kindly.ai under _Connect -> Publish -> Kindly Chat_.

## Install
```bash
nvm use
npm i -g gulp-cli
npm install
gulp serve
```

## Deployment

Using localhost:

```bash
gulp bundle
gulp package-solution
```

Using CDN:

```bash
gulp bundle --ship
gulp package-solution  --ship
```


## References

- [Getting started guide (Build your first SharePoint Framework Extension)](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/extensions/get-started/build-a-hello-world-extension) <- Do the four step guide
- [Enable your tenant app catalog](https://docs.microsoft.com/en-us/sharepoint/use-app-catalog)
- [Enable CDN](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/enable-microsoft-365-content-delivery-network?tabs=o365cli)
- [Github Issue on loading custom javascript in Sharepoint](https://github.com/SharePoint/sp-dev-docs/issues/1674)