# Example Licensing Portal

This is an example of how to set up a simple customer-facing license activation
portal using LicenseGen's API and React.

![screenshot](/images/License-portal.png)

The portal offers the following functionality:

- License information e.g. expiration date.
- Machine activation.
- Machine deactivation.

## Running the example

First up, configure a few environment variables:

```bash
# Your LicenseGen account ID. Find yours at https://licensegen-admin.focusapps.app/settings.
export LICENSEGEN_ACCOUNT_ID="2ed45aa2-b1e9-4ba7-83bb-a037ccf5a85e"
export LICENSEGEN_LICENSE_KEY="80246B-1DE0D3-B22291-00B387-B9C4DD-V3"
```

You can either run each line above within your terminal session before
starting the app, or you can add the above contents to your `~/.bashrc`
file and then run `source ~/.bashrc` after saving the file.

Next, install dependencies with [`yarn`](https://yarnpkg.comg):

```bash
yarn
```

Finally, boot the example portal app:

```bash
yarn start
```

The app will be available at `http://localhost:1234`.

## Demo credentials

To run on the `demo` account, run the following:

```bash
LICENSEGEN_ACCOUNT_ID=demo LICENSEGEN_LICENSE_KEY="80246B-1DE0D3-B22291-00B387-B9C4DD-V3" yarn start
```

## License key authorization

Used `License key authorization` in this case，you have to set `Authentication Strategy` of [`police`](https://licensegen-admin.focusapps.app/policies)  to `MIXED` or `License Keys`

## Fingerprinting

The example stores a random UUID to local storage to identify the current
device. This can be changed to a more sophisticated fingerprinting
strategy if required, e.g. device GUID or hardware ID.

To reset your fingerprint, run the following in the browser console:

```js
localStorage.clear()
```

This will allow you to test activation limits more easily.

## Questions?

Reach out at [licensegen@focusapps.app](mailto:licensegen@focusapps.app) if you have any
questions or concerns!
