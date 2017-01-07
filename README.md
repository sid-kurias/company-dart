# company-dart
Company mode autocompletion for Dart

 Add something similar to your init file

    (add-hook 'dart-mode-hook (lambda ()
     (set (make-local-variable 'company-backends)
      '(company-dart (company-dabbrev company-yankpad)))))

 Dart completion will be invoked only after the "." character has been typed.
 For this to work company-minimum-prefix-length should be set to 0. If that
 is inconvenient you can manually invoke completion by binding (company-dart)
 to any key you like.

 While in the completion list, hitting F1 will show you the documentation for
 the selected candidate. Alternatively https://github.com/expez/company-quickhelp
 shows the documentation as a popup.

 A good source for snippets
 https://github.com/JEG2/dotfiles/tree/master/emacs.d/jeg2/snippets/dart-mode/.
 If you use yankpad, you can use the accompanying yankpad.org file for dart
 snippets. The corresponding company backend is at
 https://github.com/sid-kurias/company-yankpad

 Requires dart-mode from https://github.com/sid-kurias/dart-mode. Company-mode
 and pos-tip are the other dependencies.