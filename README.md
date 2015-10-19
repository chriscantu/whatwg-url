# whatwg-url

whatwg-url is a full implementation of the [WHATWG URL](https://url.spec.whatwg.org/) specification.

## Current State

whatwg-url is currently up to date with the URL spec up to commit [ecb120f](https://github.com/whatwg/url/tree/ecb120ffd2a72c65fc5091597fa821208998e349).

## API

The main API is the [`URL`](https://url.spec.whatwg.org/#url) export, which follows the spec.

The following methods are exported for use by places like jsdom that need to implement things like [`HTMLHyperlinkElementUtils`](https://html.spec.whatwg.org/#htmlhyperlinkelementutils). They operate on an "internal URL" or ["URL record"](https://url.spec.whatwg.org/#concept-url) type.

- [URL parser](https://url.spec.whatwg.org/#concept-url-parser): `parseURL(input, { baseURL, encodingOverride })`
- [Basic URL parser](https://url.spec.whatwg.org/#concept-basic-url-parser): `basicURLParse(input, { baseURL, encodingOverride, url, stateOverride })`
- [URL serializer](https://url.spec.whatwg.org/#concept-url-serializer): `serializeURL(urlRecord, excludeFragment)`
- [Host serializer](https://url.spec.whatwg.org/#concept-host-serializer): `serializeHost(hostFromURLRecord)`
- [Serialize an integer](https://url.spec.whatwg.org/#serialize-an-integer): `serializeInteger(number)`
- [Origin](https://url.spec.whatwg.org/#concept-url-origin) [Unicode serializer](https://html.spec.whatwg.org/multipage/browsers.html#unicode-serialisation-of-an-origin): `serializeURLToUnicodeOrigin(urlRecord)`
- [Set the username](https://url.spec.whatwg.org/#set-the-username): `setTheUsername(urlRecord, usernameString)`
- [Set the password](https://url.spec.whatwg.org/#set-the-password): `setThePassword(urlRecord, passwordString)`.
