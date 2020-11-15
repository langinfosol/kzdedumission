
Clone the theme repository::

    git clone https://github.com/langinfosol/kzdedumission.git

Render your theme::

    tutor config render --extra-config ./kzdedumission/config.yml ./kzdedumission/theme "$(tutor config printroot)/env/build/openedx/themes/kzdedumission"

Rebuild the Openedx docker image::

    tutor images build openedx

Restart your platform::

    tutor local start -d

You will then have to enable the "kzdedumission" theme:

    tutor local settheme indigo localhost studio.localhost \
        $(tutor config printvalue LMS_HOST) $(tutor config printvalue CMS_HOST)

Upgrade
-------

To upgrade the kzdedumission theme from a previous version, simply pull the changes from the git repository::

    cd kzdedumission/
    git pull

Then run the commands above starting from ``tutor config render...``.


License
-------

This work is licensed under the terms of the `GNU Affero General Public License (AGPL)
