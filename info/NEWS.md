
# Table of Contents

1.  [Version 20.4.0: 2020-04: Updated for Ansys 2020R1](#org067245d)
2.  [Version 20.3.0: 2020-03: Melpa installation](#org2b9f37e)
3.  [Version 20.2.0: 2020-03: Updated keywords to Ansys v195](#orgd5c2edb)
4.  [Version 20.1.1: 2020-02: Bugfix release](#org02008b6)
5.  [Version 20.1.0: Released  2020-02](#org1d2b76b)
6.  [Version 162-1, not yet released, targeted for Sep 2015](#orgc8b2978)
7.  [Version 16.1.1 July 2015](#org4eb4ca0)
8.  [Version 15.0.1 Aug 2014](#org687ad15)
9.  [Version 14.5.2  Mar 2013](#org42af51a)
10. [Version 14.5.1 Sep 2012](#org779bf16)
11. [Version 14.0.1 June 2012](#orgfda40bd)
12. [Version 13.0.1 March 2011](#org7a92d49)
13. [Version 12.0.1 Dec 2010](#org8ca1bb2)
14. [Version 11.0.2 Nov 2009](#org6bceaff)
15. [ansys-mode.el 11.0.1 2009 in comparison to ansys-mod.el:](#org4e7527f)

Copyright (C) 2006 - 2020  H. Dieter Wilhelm, GPL V3


<a id="org067245d"></a>

# Version 20.4.0: 2020-04: Updated for Ansys 2020R1

-   Updated keywords to Ansys 2020R1 (v201)
-   Added documentation in GNU Info format and modified the menu
    entry APDL-Mode Online Documentation to APDL-Mode Documentation
    (C-c C-h) which points to the GNU-Emacs internal Info Viewer.
-   Added a menu entry for displaying the user's taken licenses
-   Files with the suffixes ".mac", ".dat" and ".inp" are openend in
    apdl-mode without further user configuration.
-   Added additional keys for the license status functions


<a id="org2b9f37e"></a>

# Version 20.3.0: 2020-03: Melpa installation

-   You can now install APDL-Mode from the [Melpa](https://melpa.org/) package archive!
-   Added a new menu entry for browsing interactively the
    documentation for keywords
-   Added new function template the menu
-   EWW browser for the local help is now opening in a different
    "Window" and is not hiding the APDL buffer any longer
-   Added Ruler Mode to the helper modes
-   Added customisation section for Worbench / Discover Aim templates
-   Improved initialisation of Ansys installation dependent
    parameters


<a id="orgd5c2edb"></a>

# Version 20.2.0: 2020-03: Updated keywords to Ansys v195

-   Added a template preview system for Worbench \`Command (APDL)'
    objects with the keybinding \`C-c C-w' (this keybinding was
    formerly used for starting WorkBench).
-   Improved the automated configuration of Ansys installation
    dependent components
-   Made M-? (the parameter help) robuster, command names can now be
    changed when the help overlay is visible
-   Updated documentation and completions for keywords, elements,
    etc. to v195 (some to v201)
-   A-M can call a browser for the Ansys online-help (you don't have
    to install the local Ansys help package, though it is advisable
    because of speed reasons.


<a id="org02008b6"></a>

# Version 20.1.1: 2020-02: Bugfix release

-   Renamed apdl-browse-apdl-guide to apdl-browse-ansys-apdl-manual
-   Improved configuration docu
-   Enabled EWW (and other browsers) as a "help viewer"


<a id="org1d2b76b"></a>

# Version 20.1.0: Released  2020-02

-   Changed the name to APDL-Mode
-   Changed version naming scheme (package.el format)
-   Installation now with Emacs' packageing system
-   Added key-bindings to the license buffer ****Licenses**** (C-c C-l)
    o - occur search
    g - refresh license status
    q - bury the license buffer
    Q - quit license buffer
-   Better warning for C-c C-b when A-M is not configured


<a id="orgc8b2978"></a>

# Version 162-1, not yet released, targeted for Sep 2015

-   Sending code to the ANYSClassics GUI is now possible as well, not
    only to the restricted interactive solver (currently only on
    GNU-Linux and Unix with C-c C-j, C-c C-u, C-c C-c).
-   Checking available licenses - in a fast and simple way - is now
    also available on Windows platforms with "C-c C-l".
-   Reorganised and simplified the installation and configuration.
    Made the initialisation defaults more intelligent,
    i. e. searching for installation paths with environment
    variables, etc.
-   New customisation variable \`ansys-parameter-help-duration' for
    adjusting the display duration of the
    \`ansys-show-command-parameters' overlay.
-   Reorganised and improved the menu items, separated general Ansys
    tasks from APDL coding with two main menu Entries: A-Mode and
    Ansys.
-   New functions: Reading the original APDL guide and Ansys-Mode's
    documentation in a Browser, opening an empty buffer in
    Ansys-Mode, ansys-start-launcher, ansys-start-classics, &#x2026;
-   The command \`C-c C-j' does now recognise blocks (APDL loops and
    control structures), which is to say it copies or sends complete
    logical blocks to the interpreter instead of only the current
    code line.
-   Changed Ansys-Mode's versioning scheme from 16.2.1 to 162-1


<a id="org4eb4ca0"></a>

# Version 16.1.1 July 2015

-   The command \`ansys-show-command-parameters' (M-?) does
    additionally count the number of parameters and visualise at
    which parameter position the cursor currently is.  This tool-tip
    can now be switched off with a prefix argument of zero.
-   The command \`ansys-send-to-ansys-and-proceed' (C-c C-j) is now
    interactive, i. e. after invoking this command with its key-sequence
    "C-c C-j" it can be repeated by typing just the final character "j"
    (or "C-j").
-   The command \`ansys-send-to-ansys' (C-c C-c) grabs now the current
    paragraph, when there is no region marked.  And the cursor doesn't
    skip to the next code line without a prefix argument "C-u".
-   The output buffer **Ansys** of the interpreter commands might now
    reside on a another Emacs frame.
-   switched on truncation of lines for Ansys-Mode buffers, e. g. it is
    easier to read when there are many parameters in the
    ansys-show-parameter-help.
-   Extended the APDL material library which includes now creep and
    multi-linear plasticity data in matlib/ as well.
-   Is packaged with the current stable version Emacs-24.5 and updated
    for Ansys 16.  Besides the Windows version there is also now a
    source package available for compiling Emacs-24.5 together with
    Ansys-Mode.
-   Renamed README, NEWS and TODO to \*.org, fontification.mac to
    example.mac.  Included an example.dat and example.anf


<a id="org687ad15"></a>

# Version 15.0.1 Aug 2014

-   Added an example of an Ansys material library
-   C-c C-c (ansys-send-to-ansys) doesn't skip to the next code line any
    longer but remains in the code line. The former behaviour borrows
    the new function C-c C-j (ansys-send-to-ansys-and-proceed),
    executing and then skipping to the next code.
-   Improved the \`ansys-show-blabla&#x2026;
-   Highlighted now the parametric function CXABS(), which was already
    introduced in V14.
-   Updated the help, completion and highlighting functionality to V15
    And as usual: Corrected some bugs, typos and extended the templates,
    e. g. partial solutions with psolve for mass calculations.


<a id="org42af51a"></a>

# Version 14.5.2  Mar 2013

-   The unwieldy and usually uninteresting pure number blocks (the
    nblock, eblocks and cmblocks) in files with the suffix .dat are now
    hidden by default.  WorkBench creates these blocks in input files
    for the solver.  You can, off course, unhide these blocks and
    inspect them as well.
    
    Functions: \`ansys-hide-number-blocks', \`ansys-show-number-blocks',
    \`ansys-hide-region'
    
    Customising variables: \`ansys-hide-region-before-string',
    \`ansys-hide-region-after-string' and
    \`ansys-hide-region-propertize-markers'

-   Added a way for showing the current value and status of a user
    variable at point, overcoming the drawback of C-c C-v
    \`ansys-display-variables' that it is showing only the variable
    definitions and definitions coming from external files are not
    shown. You can activate this functionality (Linux only) with a
    prefix argument: C-u C-c C-v.
-   Fixed the completion and highlighting of command keywords and their
    help entries, in the previous release were unfortunately many
    keywords missing or entries incomplete.
-   As always: Enhancements and corrections for the APDL templates,
    added a beam simulation template


<a id="org779bf16"></a>

# Version 14.5.1 Sep 2012

-   Added a function (C-c C-b or "M-x ansys-browse-ansys-help") showing
    the detailed Ansys help in your web-browser for an APDL command or
    element name (also the element number is sufficient) around the
    cursor (or if that fails at the line beginning).
    
    Are you also tired of the Ansys help browser?  For example try
    searching for the \`F' APDL command, it is impossible! (update 2014:
    This has improved with the new help viewer in V15.) You have to pick
    it up from the alphabetical command list. Likewise when you are
    searching for an incomplete keyword, no hint, no completion,
    nothing!  Finding and browsing relevant APDL documentation is still
    cumbersome and too slow.
    
    As a highlight of this release you can now read immediately the
    detailed Ansys help in your web browser for **all** APDL command AND
    element names around the cursor (or for the first command in the
    current line if that fails to be valid keyword).  You may input your
    search string also interactively, including its completion to Ansys
    help keywords and of certain help categories, like \`Release Notes'
    and such. This is an ideal complement to Ansys-Mode's in-built
    \`command syntax help'.

-   The function \`ansys-start-ansys' is now available under Windows as well
    and starts the APDL product launcher under this platform.
-   When calling \`ansys-browse-ansys-help' and
    \`ansys-show-command-parameters' (M-? - the in-built \`command syntax
    help') with a prefix argument for interactively entering a command
    name, the name is now completable.  And in the non-interactive mode
    both functions working also for APDL commands which are commented
    out as well (only for the first command in case of
    \`ansys-show-command-parameters').
-   Also the input of \`ansys-query-ansys-command' (C-c C-q) is now
    completable to all current Ansys commands and with an optional
    prefix argument the current code line is copied as the initial
    input.
-   Improved the introductory and the in-depth tutorial and extended the
    documentation with an APDL and syntax highlighting reference in HTML
    and PDF. (To some degree syntax highlighted in the PDF version as
    well)
-   Values of the \`<sub>RETURN</sub>' variable are now documented in the function
    \`ansys-skeleton-information'
-   \`ansys-next-code-line' and \`ansys-previous-code-line' (M-n, M-p) are
    now skipping over node and elements blocks, which are only pure
    number blocks.  They are now alternatives to
    \`ansys-number-block-start' C-c { and C-c } respectively
-   Removed bug in customisation system and dropped 32 bit Ansys support
    in line with the Ansys OS
    [<https://www.ansys.com/Support/Platform+Support> strategy] for 2013.
-   Described a poor man's round() workaround in ansys-template-function
    under the nint() entry


<a id="orgfda40bd"></a>

# Version 14.0.1 June 2012

-   Enhanced the documentation, included is now an introductory tutorial
    \`ansys-mode<sub>tutorial.pdf</sub>' and a hands-on tutorial
    \`APDL<sub>tutorial.pdf</sub>'
-   Added a timer for getting rid of the parameter help overlays after
    some time interval (1 min) without reusing the parameter help
-   Added a (customisable) variable \`ansys-no-of-processors' and
    function with the same name for specifying the number of processors
    for an Ansys multiprocessor run
-   Activated outline-minor-mode and auto-insertion (in default<sub>el</sub>)
-   Extended mode commands, templates and removed typos mainly in
    ansys-template.el. For example added all \*get functions in the
    ansys-skeleton-function template
-   Added a custom variable the corresponding function
    ansys-ansysli-servers for specifying the ansys interconnect license
    servers
-   Added a new shortcut and menu entry isometric view
-   Applied sensible defaults to ansys-lmutil-program, ansys-program and
    ansys-help-program, for most needs it should now be enough just to
    set the used ansys version (ansys-current-ansys-version, if it is
    not 140, see the example configuration file default<sub>el</sub>) and maybe
    additionally the installation directory (ansys-install-directory).


<a id="org7a92d49"></a>

# Version 13.0.1 March 2011

-   Added support for aligning whole sections of Ansys variable
    definitions, both in the Ansys menu and as a keyboard shortcut 'C-c
    C-a'
-   Enhanced ansys-display-skeleton with an optional argument for
    inserting the respective skeleton in the APDL buffer.
-   Enhanced some "interactive" code templates with lists for completing
    the input and sensible defaults
-   Refined some abbreviation definitions and focused the display of
    abbreviations to the mode specific ones
-   Fixed insert pair functions, like 'C-c %'
-   Changed keyboard shortcut for calling the Ansys help to 'C-c C-h'
-   Updated keyword list, deprecated elements, undocumented commands,
    etc. to release 13.0 of Ansys, as usual.


<a id="org8ca1bb2"></a>

# Version 12.0.1 Dec 2010

-   Some new graphics commands like ansys-zoom-in, -zoom-out,
    -move-left, -right, -up, -down, etc.
-   The lisp code had to be split up for better maintenance, the code
    files for are now provided in an archive together with their
    compiled state for speed reasons.
-   Reworked the highlighting mainly for the sake of speed.  There
    are now highlighting levels to choose from, offering
    e. g. highlighting of deprecated element types in a warning-face,
    deprecated Ansys \* comments and so on
-   Updated and improved the readability of the mode's help and the
    README file
-   The output from the LMUtil license status tool (C-c C-l) is now
    filtered on UNIX to be more concise.
-   The \`ansys-send-to-ansys' (C-c C-c) and the ansys-copy-or-send-above
    (C-c C-u) commands are now generalised so that they are also doing
    some useful stuff without a running Ansys interpreter process (they
    copy in that case the cursor line/the chosen region and copy from
    the file beginning to the cursor line, respectively, to the
    clipboard).  Given a prefix argument to these commands, the cursor
    won't move to the next code line.
-   The completion of Ansys keywords is reworked and has improved.  Ansys
    symbols are now completed in 3 ways: Up-case, down-case and
    capitalise.
-   New: Added tool-tips to all Ansys menu entries.  Activated or
    deactivated menu entries according to the context
-   Ansys mode tries to gather information from the OS environment when
    the variable \`ansys-license-file' is not set by the user and uses
    now Ansys standard names as default values for some more variables.
-   The variables in the variable summary are now sorted according to
    their first occurrence and not any longer in "definition types".  Now
    component names are included with the variable highlighting.
-   Added menu entry for reloading Ansys Mode for the case when certain
    customisation options in the code files itself are changed and
    require a code reloading to take effect.
-   Ansys mode changes some Emacs default behaviour to smooth the
    transition from other editors


<a id="org6bceaff"></a>

# Version 11.0.2 Nov 2009

-   Enabled the preview of code templates or fragments (called
    skeletons in this mode, please inspect \`ansys-display-skeleton').
-   Removed "buffer has no process" bug when killing an ansys-mode
    buffer.
-   Submitting interactively Ansys commands (via mini-buffer query, not
    only as written in a macro file) to the solver process,
    ansys-query-ansys-command (C-c C-q).


<a id="org4e7527f"></a>

# ansys-mode.el 11.0.1 2009 in comparison to ansys-mod.el:

-   New: Provides Ansys command parameter- and syntax help.
-   New: Offers Ansys process management: Acquiring license server
    information in a buffer Starting and stopping asynchronously
    Ansys runs.  Sending code lines to running Ansys process (sort of
    code debugging facility) and getting the output into a buffer.
-   New: Experimental highlighting of user defined variables.
    Redefinition and clearing of variables is not yet taken into
    account.
-   New: Emacs customisation facility is available for the new Ansys
    mode group.
-   New: Emacs outline-minor-mode is readily available in conjunction
    with this mode.
-   Completions of Ansys commands are now case-sensitive, with
    additional completion of function and element names.
-   Previously defined skeletons are fully functional now, new ones
    are added and enabled with the abbreviation and auto-load
    facilities of Emacs 22.
-   Ansys' interpreter's disregard of any capitalisation is now fully
    taken into account in the highlighting.
-   The apostrophe "'" is now assigned as the Ansys string and the
    value of character parameters delimiter and not wrongly """;
    the strings are highlighted accordingly.
-   The dollar sign "$" is now emphasised as the Ansys condensed
    input character (multiple Ansys commands in one line).
-   The colon ":" is now emphasised as the Ansys colon do loop
    character ("(x:y:z)" means from x to y, in z steps, z is equal to
    one as default).  For example: "n,(1:6),(2:18:2)" runs 6 loops.
    Colon loops are working also with real values: k,,(2.5:3:0.1) and
    with array parameters: k,,A(1:100), but the latter is an
    undocumented feature. Since ansys 11.0 the colon looping is also
    working with \*GET functions (example: A(1:5)=NX(1:5))). A ":"
    indicates also a beginning of a label for the \*GO and \*IF
    command.
-   "%" is now distinguished as the Ansys parameter substitution
    and format specifier character.
-   The ampersand "&" is now correctly highlighted as the only
    available Ansys continuation character applicable to the format
    commands (\*MSG, \*MWRITE, \*VREAD and \*VWRITE) command and the
    subsequent format strings of the command are highlighted.
-   New: " **" (<SPC> before \`**') is indicated as an (Ansys deprecated)
    comment sign e. g.: %% a = 3 \*\*4 %% results in "a" having the value
    3, whereas %% a = 3\*\*4 %% sets "a" to 81!
-   New: A line beginning with a comma is indented to the length of the
    last non slash or asterisk command as a reminder that the Ansys
    solver interprets this as a space holder for the last command
    keyword (the Ansys default command concept).
-   Extended documentation, code cleaning and simplification of commands
    (e.g. comment handling) with the application of standard Emacs 22
    facilities among other things.
