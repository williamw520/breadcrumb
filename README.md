Breadcrumb for Emacs
====================

# About
Breadcrumb is an add-on module for Emacs letting you to set a series of quick bookmarks
in the file buffers, and jump back to them quickly.

When editing and navigating a large number of files in Emacs, it's often easy to 
get lost and forget which files and where in the files you have visited along the way.
Breadcrumb let you leave "breadcrumb" bookmarks along the way.  Going back is easy -
just follow the trail of breadcrumbs to jump back to the exact locations in the files.

# Feature Overview
* Set bookmarks with minimal hassle.  One key-stroke.
* Bookmarks are global across buffers.
* Jump to and cycle through bookmarks in multiple buffers quickly.  One key-stroke.
* Jumping and cycling through the bookmarks in the local buffer is supported.
* Bookmarks are persistent when exiting and staring Emacs.
* Different types of buffer can be bookmarked: file, dired, info, and system.
* Integrated with find-tag and tags-search to set bookmark automatically.
* Bookmark list menu allows interactively listing and managing of bookmarks.
* Interactively visit bookmarks in the other window in the bookmark menu.

# Installation
Put breadcrumb.el in your load-path.  The load-path is usually ~/elisp/.
It's set in your .emacs, like this:

    (setq load-path (append (list (expand-file-name "~/elisp")) load-path))

Add the following to your .emacs startup file.

    (require 'breadcrumb)

# Configuration

Assign the commands to some keys in your .emacs file.

One example below assigns a set of keys to the breadcrumb bookmark functions.

    (global-set-key [(shift space)]         'bc-set)            ;; Shift-SPACE for set bookmark
    (global-set-key [(meta j)]              'bc-previous)       ;; M-j for jump to previous
    (global-set-key [(shift meta j)]        'bc-next)           ;; Shift-M-j for jump to next
    (global-set-key [(meta up)]             'bc-local-previous) ;; M-up-arrow for local previous
    (global-set-key [(meta down)]           'bc-local-next)     ;; M-down-arrow for local next
    (global-set-key [(control c)(j)]        'bc-goto-current)   ;; C-c j for jump to current bookmark
    (global-set-key [(control x)(meta j)]   'bc-list)           ;; C-x M-j for the bookmark menu list

Another sample set of bindings similar to MS Visual Studio bookmark setting.

    (global-set-key [(control f2)]          'bc-set)
    (global-set-key [(f2)]                  'bc-previous)
    (global-set-key [(shift f2)]            'bc-next)
    (global-set-key [(meta f2)]             'bc-list)

