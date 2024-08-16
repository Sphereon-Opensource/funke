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
overhaul and functionalities required by the ARF have been mostly implemented. A [Relying Party demo](https://funke.demo.sphereon.com) accepting mDL/mdocs and SD-JWTs of which the
presentation definitions can be managed with the [web wallet frontend](https://github.com/Sphereon-Opensource/web-wallet/) has been provided

Quick links:
- Mobile wallet: 
  - [iOS & Android code](https://github.com/Sphereon-Opensource/mobile-wallet/tree/funke)
- Relying Party Demo
  - [Demo portal](https://funke.demo.sphereon.com)
  - [Agent (backend) code](https://github.com/Sphereon-Opensource/web-wallet/tree/develop/packages/agent). See also the [general repo/readme](https://github.com/Sphereon-Opensource/web-wallet/)
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


