# Multi-Page Dash App Plugin

A plugin to simplify creating multi-page Dash apps.

Will likely be an official part of the `dash` library in the future.

### Background

The goal of this plugin is to remove as much boilerplate as possible when creating multi-page Dash apps.

This plugin allows users to simply place their layouts in `pages/` and call `dash.register_page` with the desired URL path of that page.

This plugin will automatically:
- Create the URL routing callback
- Add page information to `dash.page_registry` that can be used when creating navigation bars
- Set `validate_layout` accordingly so that users don't need to `suppress_callback_exceptions`
- Set the order of `dash.page_registry` based off `order`  and the filename
- Set `<title>` and `<meta description>` and their social media equivalents accordingly
- Set a clientside callback to update the `<title>` as you navigate pages with `dcc.Link`
- Set the meta image accordingly based off of images available in assets

### Usage

As a user, see `app.py` and the files in the `pages/` folder.

For the `register_page` docstring, see the `pages_plugin.register_page` docstring.