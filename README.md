## kindly-chat-extension

This is an example Sharepoint extension to add Kindly Chat to Sharepoint. The approach is based on [a migration path for legacy sharepoint scripts](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/extensions/guidance/migrate-from-usercustomactions-to-spfx-extensions).

Use this code as a basis for your own Sharepoint installation. To deploy you first need update your bot key in `src/extensions/kindlyChatExtension/KindlyChatExtensionApplicationCustomizer.ts`. Locate your bot key on app.kindly.ai under _Connect -> Publish -> Kindly Chat_.

## Install
```bash
nvm use
npm i -g gulp-cli
npm install
gulp serve
```

## Deployment

See [step three](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/extensions/get-started/serving-your-extension-from-sharepoint) and [four](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/extensions/get-started/hosting-extension-from-office365-cdn) in the getting started guide for detailed steps.

Using localhost to test:

```bash
gulp bundle
gulp package-solution
```

Using CDN:

```bash
gulp bundle --ship
gulp package-solution  --ship
```

Upload the `.sppkg` file under `sharepoint/solution` to your App catalog in your Sharepoint Admin interface.


## References

- [Getting started guide (Build your first SharePoint Framework Extension)](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/extensions/get-started/build-a-hello-world-extension) <- Do the four step guide
- [Enable your tenant app catalog](https://docs.microsoft.com/en-us/sharepoint/use-app-catalog)
- [Enable CDN](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/enable-microsoft-365-content-delivery-network?tabs=o365cli)
- [Github Issue on loading custom javascript in Sharepoint](https://github.com/SharePoint/sp-dev-docs/issues/1674)