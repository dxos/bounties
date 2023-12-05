# Composer Native

A "more native" app experience for Composer. The goal will be to release three native apps, which, listed in priority are 1) iOS mobile, 2) Mac desktop, and 3) Android mobile.

## Goals

### Add app features

#### Platform agnostic features

These are features that will apply to all three native platforms we are targeting.

- Use [Socket Supply Co](https://socketsupply.co/) to wrap existing Composer App.
- Get the client working inside of the SSC runtime. There are currently issues that prevent the client from properly working. Josiah is currently [reworking the architecture](https://github.com/orgs/dxos/discussions/4685) so that it possibly will be easier to get running in SSC.
- Add support for [Universal Links](https://developer.apple.com/ios/universal-links/) on iOS and [Deep Links](https://developer.android.com/training/app-links/deep-linking) on Android so that documents from the web can be opened in the app. This is essential to the process for accepting invitations from QR codes. SSC does not currently support app links out of the box, but they have [an issue](https://github.com/socketsupply/socket/issues/790) open for it with notes on how it could be possibly done.
- Ensure that the following user workflows can be completed:
  - Scan QR code with phone camera to accept invitation to connect to account
  - Scan QR code with phone camera to accept invitation to join a shared space
  - Data should persist after device is restarted

#### Platform specific features

These are features that add features available on specific native platforms.

##### Mac Desktop

- Add native menu items that would open specific views in the app, such as Settings.
  - SSC has a [config option for this](https://socketsupply.co/apis/#application_setsystemmenuoptions)
  - Routing might have to be adjusted in Composer to show these views based on a URL or URL parameter.
- Add a global keyboard shortcut that will open Composer in a command pallette state.
  - A MVP version of this could be a local shortcut that opens when Composer is already open and in focus. SSC already has support for this.
  - SSC does not currently have support for global shortcuts. We would have to find a way to add them ourselves, possibly working with the SSC team on this. [This library](https://github.com/soffes/HotKey) might give us a place to start. The best user experience might include a menubar helper application that launches at system boot that would listen for the shortcut.
  - Ideally for user experience, this global shortcut could be user configured, in case that they have an existing global shortcut that conflicts with the default.

### Publish to app stores

We want to publish to the iOS App Store, the Mac App Store, and the Google Play Store. We will have to make sure the following goals are met for each app store:

- Research the release process so that future updates of the JS bundle do not need a full review.
- Prepare assets and content for release to the respective app stores: 
  - App description
  - App metadata (Company, contact info, category)
  - Screenshots
  - Properly sized icons
- Submit the applications to the respective app stores for review and and address any issues that the reviewers bring up in the process.
