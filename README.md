# NAME

Appium - Perl bindings to the Appium mobile automation framework (WIP)

# VERSION

version 0.02

# SYNOPSIS

    my $appium = Appium->new(caps => {
        app => '/url/or/path/to/mobile/app.zip'
    });

    $appium->hide_keyboard;
    $appium->quit;

# DESCRIPTION

Appium is an open source test automation framework for use with native
and hybrid mobile apps.  It drives iOS and Android apps using the
WebDriver JSON wire protocol. This module is a thin extension of
Selenium::Remote::Driver that adds Appium specific API endpoints and
Appium-specific constructor defaults.

It is woefully incomplete at the moment. Feel free to pitch in!

# METHODS

## contexts ()

Returns the contexts within the current session

    $appium->contexts;

## current\_context ()

Return the current active context for the current session

    $appium->current_context;

## switch\_to->context ( $context\_name )

Switch to the desired context for the current session

    $appium->switch_to->context( 'WEBVIEW_1' );

## hide\_keyboard( key\_name|key|strategy => $key\_or\_strategy )

Hides the software keyboard on the device. In iOS, you have the option
of using \`key\_name\` to close the keyboard by pressing a specific
key. Or, you can use a particular strategy. In Android, no parameters
are used.

    $appium->hide_keyboard;
    $appium->hide_keyboard( key_name => 'Done');
    $appium->hide_keyboard( strategy => 'tapOutside');

# SEE ALSO

Please see those modules/websites for more information related to this module.

- [http://appium.io](http://appium.io)
- [Selenium::Remote::Driver](https://metacpan.org/pod/Selenium::Remote::Driver)

# BUGS

Please report any bugs or feature requests on the bugtracker website
https://github.com/gempesaw/Appium-Perl-Client/issues

When submitting a bug or request, please include a test-file or a
patch to an existing test-file that illustrates the bug or desired
feature.

# AUTHOR

Daniel Gempesaw <gempesaw@gmail.com>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2014 by Daniel Gempesaw.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
