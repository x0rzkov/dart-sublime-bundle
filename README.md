# Dart bundle for Sublime

This bundle provides basic Dart support for Sublime Text. This bundle supports
both Sublime Text 2 and the Sublime Text 3 Beta. The following features are
currently provided:

* Syntax highlighting.
* Preferences for comments so that you can use CMD-/ to (de)comment source
  lines.
* Some snippets for inserting common Dart code.
* dart2js support through Sublime's build system.
* Support for installing Pub packages.
* dartanalyzer support for Linter feedback.

The bundle identifies dart source by the file extension (.dart).

For an overview of installing and working with this plugin, check out our
[introductory video][6].

PRE-REQ
=======

You will need the Dart SDK before you use the full features of this bundle.

1. [Download and install the Dart SDK][sdk]
2. Ensure the SDK's `bin` directory is on your path.

INSTALLATION
============

If you are using the [Package Control][1] plugin, installation is very easy.
Open the command palette (CTRL-SHIFT-P or CMD-SHIFT-P), type 'Install' and
select 'Package Control: Install Package' from the list. Next, type 'Dart' and
select the Dart package from the list. You may need to close and reopen any Dart
files you currently have open for the syntax highlighting to activate.

To install this package manually, copy the the contents of this repository to a
new directory in the Sublime packages directory (on OSX:
~/Library/Application Support/Sublime Text 2/Packages).

For the best experience, make sure the `dart-sdk/bin` directory is on your path.
Also, add the `dartsdk_path` variable to your user settings:

    {
      "dartsdk_path" : "/Users/foo/dart-sdk"  
    }

Looking for an IDE experience? Try [Dart Editor][2],
[Dart plugin for Eclipse][3], or [Dart plugin for IntelliJ/WebStorm][4].

BUILD SYSTEM USAGE
==================

  - CTRL+B or CMD+B will run the dart2js compiler on the current open file.
  - Open the command pallete (CTRL-SHIFT-P or CMD-SHIFT-P), type 'Dart' to see
    other Dart commands: `Run`, `Analyzer`, `pub install`, `pub update`.

LINTER USAGE
============
By default the dartanalyzer feedback is turned off.  If you would like to use this feature you will need to change the `dartlint_active` setting to `true`.

    {
        ...
        
        "dartlint_active" : true, 
        
        ...
    }

The linter will run when documents are loaded, and when they are saved.  If you would like to change this behaviour you can change either of these settings to `false` to turn them off:

    {
    	...
    	
    	"dartlint_on_load" : true,
    	"dartlint_on_save" : true,
    	
    	...
    }

Highlight colors can be customized by changing the `dartlint_underline_color_error`, `dartlint_underline_color_warning`, and `dartlint_underline_color_info` settings.  

Gutter icons can be changed with the `dartlint_gutter_icon_error`, `dartlint_gutter_icon_warning`, and `dartlint_gutter_icon_info` settings.  Icon paths must start from the Packages directory. 

Example: `"dartlint_gutter_icon_error" : "Packages/Users/Icons/error.png"`.

DEVELOPMENT
===========

Please ensure that all .tmPreferences, .tmLanguage, .tmSnippets, etc. files stay
in sync with the related [Dart TextMate repository][5].

LICENSE
=======

    Copyright 2012, the Dart project authors. All rights reserved.
    Redistribution and use in source and binary forms, with or without
    modification, are permitted provided that the following conditions are
    met:
        * Redistributions of source code must retain the above copyright
          notice, this list of conditions and the following disclaimer.
        * Redistributions in binary form must reproduce the above
          copyright notice, this list of conditions and the following
          disclaimer in the documentation and/or other materials provided
          with the distribution.
        * Neither the name of Google Inc. nor the names of its
          contributors may be used to endorse or promote products derived
          from this software without specific prior written permission.
    THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
    "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
    LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
    A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
    OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
    SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
    LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
    DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
    THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
    (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
    OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

[1]: http://wbond.net/sublime_packages/package_control
[2]: http://www.dartlang.org/editor
[3]: http://news.dartlang.org/2012/08/dart-plugin-for-eclipse-is-ready-for.html
[4]: http://plugins.intellij.net/plugin/?id=6351
[5]: http://github.com/dart-lang/dart-textmate-bundle
[6]: http://news.dartlang.org/2013/02/using-dart-with-sublime-text.html
[sdk]: http://www.dartlang.org/tools/sdk/
