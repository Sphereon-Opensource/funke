<!--suppress HtmlDeprecatedAttribute -->
<h1 align="center">
  <br>
  <a href="https://www.sphereon.com"><img src="https://sphereon.com/content/themes/sphereon/assets/img/logo.svg" alt="Sphereon" width="400"></a>
  <br>SPRIND Funke - Wallet 
  <br>
</h1>

Welcome to an overview of the most important components and deliverables of the SPRIND Funke.

**Phase 2**
During phase 2, we have overhauled a part of the UX. See also the [Design and UX rationale](./pdf/Funke%20stage%202%20-%20Design%20rationale.pdf) that
explains choices made. We have implemented activity histories, contact details and trust establishment warnings/notifications. We have enabled and
integrated assistive technologies, including a multi-modal (text and speech) conversational User Interface that acts both as a chatbot that you can
ask questions, as
well as an assistant to execute actions on your behalf. The assistant can have both text and speech input, and provide text and speech output. You can
change the language if you want as well. It currently is limited to the issuance process and the credential details screen. However on those screens
it is fully context aware.

We have the basics of an anomaly detection plugin. It handles fetching resource from the internet, and performs an on-device country/continent
lookup. We will use this for a trust score in the near future.

We have integrated OpenID Federation for trust establishment. We also us it to fetch the signed metadata for Issuers or RPs if present. Right now the
wallet assumes it has a list of trusted Certificates and is part of 2 test federations. This means it will show a warning for any other party you will
be interacting with.

**Phase 1 (old)**
During phase 1, work on our [mDL/mdoc](https://github.com/Sphereon-Opensource/mdoc-cbor-crypto-multiplatform/tree/develop) library has progressed.
The [OID4VC libraries](https://github.com/Sphereon-Opensource/OID4VC) have been updated to the latest spec versions. Support for SD-JWTs and mDL/mdocs
has been added to the SDK and more changes have been made as one can see below.

Most importantly our Open-Source [mobile wallet](https://github.com/Sphereon-Opensource/mobile-wallet/tree/funke) for iOS and Android has had a UI/UX
overhaul and functionalities required by the ARF have been mostly implemented. A [Relying Party demo](https://funke.demo.sphereon.com) accepting
mDL/mdocs and SD-JWTs of which the
presentation definitions can be managed with the [web wallet frontend](https://github.com/Sphereon-Opensource/web-wallet/) has been provided

Quick links:

- Mobile wallet:
    - [iOS & Android code](https://github.com/Sphereon-Opensource/mobile-wallet/tree/funke)
    - [Design and UX rationale](./pdf/Funke%20stage%202%20-%20Design%20rationale.pdf)
    - Guides:
        - [Onboarding flow guide](./pdf/Guide%20-%20Sphereon%20Wallet%20Onboarding%20Flow%20with%20eID.pdf)
        - [Using the wallet guide](./pdf/Guide%20-%20Using%20the%20Sphereon%20Wallet.pdf)
- Issuer and RP Demo
    - [Demo Issuer portal](https://issuer.funke.demo.sphereon.com/issuer)
    - [Demo Relying Party portal](https://funke.demo.sphereon.com)
    - [Agent (backend) code](https://github.com/Sphereon-Opensource/web-wallet/tree/develop/packages/agent). See also
      the [general repo/readme](https://github.com/Sphereon-Opensource/web-wallet/)
    - [Frontend code](https://github.com/Sphereon-Opensource/OID4VC-demo)

## Phase 2 links

- [Experimental OID4VP SD-JWT support in ISO 18013-5 documentation](https://github.com/Sphereon-Opensource/mdoc-cbor-crypto-multiplatform/blob/develop/sphereon-kmp-mdoc-core/Experimental-OID4VP-18013-5.MD)
- [Credential and issuer branding](https://github.com/Sphereon-Opensource/UI-Components/tree/develop/packages/credential-branding)
- [SD-JWT VC type metadata](https://github.com/Sphereon-Opensource/SSI-SDK/blob/develop/packages/ssi-types/src/types/sd-jwt-type-metadata.ts)
- [OpenID Federation multiplatform](https://github.com/Sphereon-Opensource/OpenID-Federation/tree/develop)
  and [client](https://github.com/Sphereon-Opensource/OpenID-Federation/tree/develop/modules/openid-federation-client/src/commonMain/kotlin/com/sphereon/oid/fed/client)

## Phase 1 links

- SDK
    - [General SDK code](https://github.com/Sphereon-Opensource/SSI-SDK)
    - [Cryptographic SDK extension code](https://github.com/Sphereon-Opensource/SSI-SDK-crypto-extensions)
    - New modules (phase 1):
        - [Key Management System with SSCD abstraction](https://github.com/Sphereon-Opensource/SSI-SDK-crypto-extensions/tree/develop/packages/kms-musap-rn)
        - [Uniform internal and external identifier/key resolution](https://github.com/Sphereon-Opensource/SSI-SDK-crypto-extensions/tree/develop/packages/identifier-resolution)
        - [JWT/JWS signing service using unified identifiers](https://github.com/Sphereon-Opensource/SSI-SDK-crypto-extensions/tree/develop/packages/jwt-service)
        - [mDL/mdoc and X.509 module](https://github.com/Sphereon-Opensource/SSI-SDK/tree/develop/packages/mdl-mdoc)
        - [SD-JWT module](https://github.com/Sphereon-Opensource/SSI-SDK/tree/develop/packages/sd-jwt)
        - [Credential store for (SD-)JWTs, mDL/mdoc credentials and presentations](https://github.com/Sphereon-Opensource/SSI-SDK/tree/develop/packages/credential-store)
- Low level libraries with significant updates
    - [mDL/mdoc, cose, cbor multiplatform library](https://github.com/Sphereon-Opensource/mdoc-cbor-crypto-multiplatform)
    - [OID4VC (OID4VCI, OID4VP, SIOPv2)](https://github.com/Sphereon-Opensource/OID4VC)
    - [Musap react-native SSCD abstraction](https://github.com/Sphereon-Opensource/musap-react-native)

# Testing

**People testing the Funke version of the wallet (0.4.x) should not use the public available versions in the stores (0.2.x/0.3.x) as these versions of
the wallet do not have the required functionalities for the Funke!**

## iOS

Since we wanted to skip any Apple reviews which are likely to become problematic as they cannot use all features, because of the IP and NFC
requirements, we decided to put
people in the internal test track. That means that people will first have to accept the invite to join the internal test track. Only then can we add
them to the wallet team for them
to have access. We also publicly release versions, but these are always a bit later then the internal test track versions.

## Android

People should have gotten an invite for internal testing. Contrary to iOS that should lead directly to being able to install/use the 0.4.0 version of
the app. If that doesn't work then this is a direct link for internal testing: https://play.google.com/apps/internaltest/4701374210629215554
Sometimes during an update Google shows the old/store version for the test track (2.2). Do not use that version as it will not contain any of the
Funke functionality. It needs to be a 0.4.x version

## Changelog

### Phase 2

#### 2024-12-03

Second release for phase 2 (0.4.14)

- Complete overhaul of Signature validation. Previously we relied on react-native-quick-crypto and crypto.subtle in React Native. Which is known to
  not be fully
  implemented. Changed to use @noble javascript libraries, which have received multiple security audits. New implementation can be
  found [here](https://github.com/Sphereon-Opensource/SSI-SDK-crypto-extensions/blob/4ae483d7d5baf604f38dad8e5ace931612b85e2b/packages/key-utils/src/functions.ts#L755)
- The above fixes issues when signing both for SD-JWTs and Mdl/Mdocs
- New credential card list view. Demo video [here](./video/Record_2024-12-01-11-35-41.mp4)
- Add rate limiting error screen to chatbot. Unfortunately OpenAI applies ratelimits, which cannot be increased during their beta phase. Inform the
  user when it happens.


#### 2024-11-26

Initial release for phase 2 (0.4.13)

- Contact details added to contacts like terms of service, privacy policy, website, contacts (if present) for issuers and RPs
- Support for (Q)EAAs including branding of credentials and issuer
- OpenID Federation support for trust establishment, including metadata for RPs, AS, and Issuers
- Conversational UI that is context aware, can perform actions and is multi-modal (text and speech). Focussed on the issuance process for now
- Activity history
- Profile, including display of PID and derived claims
- New presentation screen

### Phase 1

#### 2024-8-29 Test Release 2

- Get both mdocs and SD-JWTs from PID issuer at the same time. Previously only the SD-JWT credential was retrieved because we didn't update the nonce
  from the response of the first credential. So although technically we could get Mdocs, we disabled them as we don't want to bother the user with
  knowledge about multiple formats.
- Presenting SD-JWTs to the RP wasn't working. This has been fixed. Mdoc presentation will follow in the next release (see TODO)
- Allow to get the PIDs from the catalog. This functionality wasn't hooked up before. Now you can get new PIDs all the time. Old PIDs will be removed
  on successful retrieval
- Only showing one PID in the list/card views no matter the format. Whenever you get the PID from the catalog it will overwrite any existing PIDs on
  success. This has always been the intention but in the first release you could end up with multiple visible PIDs.
- You can now show credential details from the credential card view. Previously this was only possible from the list view

- UX/UI polishing:
    - The Button of the pincode screen during signing of the credential request was behind the keyboard
    - The eID pincode screen was very hard to use and didn't have focus
    - Several buttons were off. For instance when deleting the wallet or deleting a credential (only in list view at the moment) the buttons were
      almost of the screen

TODO:
Many things, but we for sure want to have these in before demo day:

- Presenting mdocs isn't working at present. Finishing up some Presentation Exchange changes to make it work.
- We need to finish the C\'\' flow for presenting with NFC
- Same device flows for VP (deeplinks) aren't working, only cross-device
