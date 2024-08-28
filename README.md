<!--suppress HtmlDeprecatedAttribute -->
<h1 align="center">
  <br>
  <a href="https://www.sphereon.com"><img src="https://sphereon.com/content/themes/sphereon/assets/img/logo.svg" alt="Sphereon" width="400"></a>
  <br>SPRIND Funke - Wallet 
  <br>
</h1>

Welcome to an overview of the most important components and deliverables of the SPRIND Funke.
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
    - Guides:
        - [Onboarding flow guide](./pdf/Sphereon%20Wallet%20Onboarding%20Flow.pdf)
        - [Using the wallet guide](./pdf/Using%20the%20Sphereon%20Wallet.pdf)
- Relying Party Demo
    - [Demo portal](https://funke.demo.sphereon.com)
    - [Agent (backend) code](https://github.com/Sphereon-Opensource/web-wallet/tree/develop/packages/agent). See also
      the [general repo/readme](https://github.com/Sphereon-Opensource/web-wallet/)
    - [Frontend code](https://github.com/Sphereon-Opensource/OID4VC-demo)
- SDK
    - [General SDK code](https://github.com/Sphereon-Opensource/SSI-SDK)
    - [Cryptographic SDK extension code](https://github.com/Sphereon-Opensource/SSI-SDK-crypto-extensions)
    - New modules:
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
people in the internal test track. That means that people will first have to accept the invite to joint the internal test track. Only then can we add
them to the wallet team for them
to have access. We will keep track of that during the coming days, so people should be getting a notification once we have added them to the Funke
team (after they accepted the invite). You should have gotten an invite for the version of yesterday just now. Unfortunately Apple does not allow to
invite people directly onto a test version of the app, so it will be a two step process

## Android

People should have gotten an invite for internal testing. Contrary to iOS that should lead directly to being able to install/use the 0.4.0 version of
the app. If that doesn't work then this is a direct link for internal testing: https://play.google.com/apps/internaltest/4701374210629215554

