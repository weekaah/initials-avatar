            ___
         o$"""""$o   
       o$"       "$o
      o$  .   .    $o   . .    . ___ .   .   .    __      . .    . .  ___  .    __
     o$   |  /_\    $o  | |\ | |  |  |  /_\  |   '--.    /_\ \  / /_\  |  /_\  |__)
     o$   | /   \   $o  | | \| |  |  | /   \ |__ \__/   /   \ \/ /   \ | /   \ |  \
      o$           $o        
       o$         $o
         '"+$$$+"'


[![Build Status](https://travis-ci.org/freshbooks/initials-avatar.svg?branch=master)](https://travis-ci.org/freshbooks/initials-avatar)

An Ember CLI Addon that generates an avatar based on the initials of someone
with a first and last name.

## Installation

```
ember install initials-avatar
```

## Usage

Initials-avatar is intended to be a "default" avatar when an actual image is not
present.

If neither first or last names are present, a single initial for the company
will be displayed:

```hbs
{{initials-avatar
  firstName=userGivenName
  lastName=userFamilyName
  company=userCompany
  email=userEmail
  image=userProfileImageUrl
}}
```

There are also color classes that you can leverage to control the styling of
your different initials avatars:

```hbs
{{initials-avatar
  firstName=userGivenName
  lastName=userFamilyName
  company=userCompany
  email=userEmail
  image=userProfileImageUrl
  colorIndex=userid
  maxColorIndex=3 {{!-- you only have 3 color classes defined --}}
}}
```

You can override default color classes with:

```hbs
{{initials-avatar
  ...
  className="avatar"
  colorClassName="avatar-color"
}}
```

This will add custom css class "avatar avatar-1" to the component.


You can use a background-color directly you can pass in a `color` property.
This is useful if you want to generate colors from unique strings like emails or ids.
This background-color style will only be applied if `image` is a "falsy" value:

```hbs
{{initials-avatar
  firstName=userGivenName
  lastName=userFamilyName
  company=userCompany
  email=userEmail
  color="#f6f8fa"
}}
```

## Updating to 1.x
* Updating from 0.x to 1.x requires that your app supports [RFC 176: JavaScript Module
  API](https://github.com/emberjs/rfcs/pull/176)

Contributing
------------------------------------------------------------------------------

## Installation

* `git clone <repository-url>` this repository
* `cd initials-avatar`
* `npm install`

## Running

* `ember server`
* Visit your app at http://localhost:4200.

## Running Tests

* `ember test` – Runs the test suite on the current Ember version
* `ember test --server` – Runs the test suite in "watch mode"
* `ember try:each` – Runs the test suite against multiple Ember versions

## Building

* `ember build`

For more information on using ember-cli, visit [https://ember-cli.com/](https://ember-cli.com/).

License
------------------------------------------------------------------------------

This project is licensed under the [MIT License](LICENSE.md).
