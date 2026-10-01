<p align="center">
  <a href="https://usehardal.com/">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://imge.usehardal.com/cdn/logo/new/svg/o9vnmleauvr2t5xvn9xe.svg?raw=1">
      <source media="(prefers-color-scheme: light)" srcset="https://imge.usehardal.com/cdn/logo/new/svg/yglazyhcy7kv6053lrso.svg?raw=1">
      <img src="https://imge.usehardal.com/cdn/logo/new/svg/yglazyhcy7kv6053lrso.svg?raw=1" alt="Hardal" width="180">
    </picture>
  </a>
</p>

# Hardal Google Tag Manager Template

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) [![version](https://img.shields.io/badge/version-1.0.0-green.svg)](https://semver.org)

Send server-side events to a Hardal endpoint with this Google Tag Manager (GTM) template. Configure the project ID, API key, event fields, and optional custom domain.

## Usage

To use this GTM template, follow these steps:

1. Download the template file (`Hardal.tpl`).
2. Import the template files into your Google Tag Manager workspace.
3. Create a new Tag in GTM and choose the trigger which you want.
4. Configure the tag with the necessary parameters:

   - `projectId`: Replace this with your desired project ID.
   - `apiKey`: Replace this with your API key provided by the API service you are using.
   - `eventType`: The type of event you want to track.
   - `eventvalue`: The value associated with the event.
   - `eventData`: An object containing additional event data.

   You can also provide a `customDomain` parameter if you want to use a specific domain for the API endpoint. If not provided, it will default to 'beta.usehardal.com'.

5. Add trigger(s) to the tag to determine when the pixel should be sent.

6. Save and publish your changes in GTM.

## Example Usage

Here's an example of how the tag configuration might look like:

![example](./example/hardal-gtm-tempate-example.png)


## Example Data

The `eventData` field is text; enter the JSON properties without surrounding braces. This matches the template's request format.

```json
{
  "projectId": "12345",
  "apiKey": "YOUR_API_KEY_HERE",
  "eventType": "purchase",
  "eventvalue": "99.99",
  "eventData": "\"product\":\"Example Product\",\"quantity\":1,\"currency\":\"USD\"",
  "customDomain": "ss.example.com"
}
```
