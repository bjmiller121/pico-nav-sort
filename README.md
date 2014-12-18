# Pico Nav Sort
This is a plugin for [Pico](http://picocms.org/), a flat file PHP CMS.

## About
This plugin provides more control over the order of your navigation. It does 
this by adding several new features:
* It gives pages a weight meta property which allows you to specify the exact order 
of the menu link relative to other pages.
* To exclude a page from the navigation, don't specify a weight value for the page.
* An `active` class will be added to the link for the page you are currently on.
This can be used to style the link differently in your CSS.

## Usage
1. Download a copy of `pico_nav_sort` and add it to the `plugins` directory in
the root of your Pico install.
1. In your content meta, add a weight like so:
    
    /*
    Title: Example
    Description: This is a description
    Weight: 1
    */

1. Repeat this for each page giving each one a unique value to determine the sort
order.
1. Add the following in your theme template to render the sorted navigation:
    <ul>
      {{ nav_sort.sorted_nav }}
    </ul>
