# Example Licensing Portal

This is an example of how to set up a simple customer-facing license activation
portal using Keyrix's API and React.

![screenshot](/images/License-portal.png)

The portal offers the following functionality:

- License information e.g. expiration date.
- Machine activation.
- Machine deactivation.

## Running the example

First up, configure a few environment variables:

```bash
# Your Keyrix account ID. Find yours at https://keyrix-admin.focusapps.app/settings.
export KEYRIX_ACCOUNT_ID="e97d0572-de1c-42ae-93dd-501bf839ec38"
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
KEYRIX_ACCOUNT_ID=demo yarn start
```

Then input the following demo license key:

```
7F3DEE-75AFF5-61E976-3AF1EA-4A2013-V3
```

## License key authorization

Used `License key authorization` in this case，you have to set `Authentication Strategy` of [`police`](https://keyrix-admin.focusapps.app/policies)  to `MIXED` or `License Keys`


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

Reach out at [keyrix@focusapps.app](mailto:keyrix@focusapps.app) if you have any
questions or concerns!
