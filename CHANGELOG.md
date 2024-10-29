# Changelog

# 1.0.0 / 2024-08-25
- Promoted plugin to stable :)
- Updated to HTMX and its extensions.
- Added a helper to validate requests. Automatically handles nonce and action validation.

# 0.9.1 / 2024-07-05
- Released on WordPress.org official plugins repository.

# 0.9.0 / 2024-06-30
- Updated to HTMX 2.0.0
- More WP.org plugin guidelines compliance.

# 0.3.2 / 2024-05-26
- More WP.org plugin guidelines compliance.

# 0.3.1 / 2024-05-15
- Fixed a bug in the wp_localize_script() call. Thanks @mwender for the report.

# 0.3.0 / 2024-05-07
- WP.org plugin guidelines compliance.
- Changed hxwp_send_header_response() behavior to include a nonce by default. First argument is the nonce. Second argument, an array with the data. Check the htmx-demo.htmx.php template for an updated example.

# 0.2.0 / 2024-04-26
- Added [Alpine.js](https://alpinejs.dev/) support. Now you can use HTMX with Alpine.js, Hyperscript, or both.

# 0.1.15 / 2024-04-13
- Fixes sanitization for form elements that allows multiple values. Thanks @mwender for the report. [Discussion #8](https://github.com/TCattd/HTMX-API-WP/discussions/8).

# 0.1.14 / 2024-03-06
- Added option to add the `hx-boost` (true) attribute to any enabled theme, automatically. This enables HTMX's boost feature, globally. Learn more [here](https://htmx.org/attributes/hx-boost/).

# 0.1.12 / 2024-02-22
- Added Composer support. Thanks @mwender!
- Fixed a bug on how the plugin obtains the active theme path. Thanks again @mwender for the report and fix :)
- Added a filter to allow the user to change the default path for the HTMX templates. Thanks @mwender for the suggestion.

# 0.1.11 / 2024-02-21
- Added WooCommerce compatibility. Thanks @carlosromanxyz for the suggestion.

# 0.1.10 / 2024-02-20
- Added a showcase/demo theme to demonstrate how to use HTMX with WordPress. The theme is available at [TCattd/HTMX-WordPress-Theme](https://github.com/TCattd/HTMX-WordPress-Theme).
- hxwp_api_url() helper now accepts a path to be appended to the API URL. Just like WP's home_url().
- Keeps line breaks on sanitization of hxvals. Thanks @texorama!
- Added option to enable HTMX to load at the WordPress backend (wp-admin). Thanks @texorama for the suggestion.

# 0.1.8 / 2024-02-14
- HTMX and Hyperscript are now retrieved using NPM.
- Fixes loading extensions from local/CDN and their paths. Thanks @agencyhub!

# 0.1.7 / 2023-12-27
- Bugfixes.

# 0.1.6 / 2023-12-18
- Merged `noswap/` folder into `htmx-templates/` folder. Now, all templates are inside `htmx-templates/` folder.

# 0.1.5 / 2023-12-15
- Renamed `hxparams` to `hxvals` to match HTMX terminology.
- Added hxwp_die() function to be used on templates (`noswap/` included). This functions will die() the script, but sending a 200 status code so HTMX can process the response and along with a header HX-Error on it, with the message included, so it can be used on the client side.

# 0.1.4 / 2023-12-13
- Renamed `void/` endpoint to `noswap/` to match HTMX terminology, better showing the purpose of this endpoint.
- Better path sanitization for template files.
- Added `hxwp_send_header_response` function to send a Response Header back to the client, to allow for non-visual responses (`noswap/`) to execute some logic on the client side. Refer to the [Response Headers](https://htmx.org/docs/#response-headers) and [HX-Trigger](https://htmx.org/headers/hx-trigger/) sections to know more about this.

# 0.1.3 / 2023-12-04
- Added filters and actions to inject HTMX meta tag configuration. Refer to the [documentation](https://htmx.org/docs/#config) for more information.
- Added new endpoint to wp-htmx to allow non visual responses to be executed, vía /void/ endpoint.

# 0.1.1 / 2023-12-01
- First public release.
