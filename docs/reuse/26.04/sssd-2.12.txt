SSSD has been updated to version 2.12.

SSSD now runs under user `sssd` (instead of `root`). Make sure that `sssd` can still access secrets or integrations from its new user.

The implicit files provider and domain was removed: see <https://sssd.io/docs/files-provider-deprecation.html>.

Other changes of importance are listed upstream:

* https://sssd.io/release-notes/sssd-2.11.0.html
* https://sssd.io/release-notes/sssd-2.12.0.html
