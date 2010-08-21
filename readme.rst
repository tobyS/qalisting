=========
qalisting
=========

qalisting - code line highlighting for LaTeX lstlisting (in beamer)

This little, dirty package allows you to highlight lines in a source code
example. It is mostly used in beamer presentations, to point to certain code
potions. The 2 provided commands allow you to embed a listing and to define
highlighted lines in a simple and clean way, without messing up your LaTeX
code, the source code example and especially without loosing lstlisting
source highlighting.

Note, that this package is currently really hackish and does only work with
PHP source code, without adjustment. Use it in the current state on your own
risc! If you are advanced in LaTeX, pull requests / patches to clean this
package up and make it more flexible are highly welcome. Enjoy.

To use this package (at your own risk), do the following:

1. Download the file to your LaTeX project
2. Include the package using::

      \RequirePackage{qalisting}

3. Define some listing, like::

      \qalisting{code/my_code.php}{       % Include listing code/my_code.php.
        \only<1,3>{                       % Only on slides 1 and 3 (beamer stuff)
          \qahigh{1,3,5}                  % highlight code lines 1,3 and 5.
        }
        \only<2>{                         % Only on slide 2 (beamer)
          \qahigh{2-5}                    % highlight lines 2 to 5.
        }

Screenshot of highlighting:

.. image:: http://github.com/tobyS/qalisting/raw/master/screenshot.png
   :alt:   Screenshot of qalisting highlighted lines.
