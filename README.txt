AstroBasic
==========

AstroBasic (AB) is a scripting language made for astrology. It is built into
Planetdance, the free astrology program by Jean Cremers.

  Website and download: https://www.jcremers.com

An AB program is a plain text file with extension .ab. When you run it,
Planetdance parses it, checks it for errors and saves a compiled version
(.abc) that is used for speed. If an error is found you are put in the
editor at the offending line. Planetdance also has an integrated editor
with context help (F11), a debugger and a profiler.

A taste of the language:

  window(250, 430);
  menu(0, "Close", close);
  int i;
  char colornames[3][10] = "RED", "GREEN", "BLUE";
  for (i < 3)
    putstring(10, 20 + i * 20, colornames[i]);
  run;
  :close;
    quit;

Key points:
- statements end with ;
- variables must be declared (int, real, char), arrays start at 0
- case sensitive, all built-in commands are lower case
- labels start with : , @label calls a label as a subroutine, return goes back
- ` starts a comment, $ ... $ is a block comment
- run; waits for events (menus, buttons, timers), quit; ends the program


Contents
--------

astrobasic_help.txt   The complete language reference: syntax, variables,
                      operators, every built-in command and internal
                      variable, error messages, editor and debugger.
                      Sections are marked [name]. Parts are also in Dutch.

examples/basics       Small programs to start with
  Colors.ab           Named color constants, putstring and fill
  Julian.ab           Date to Julian day and back, edit fields
  jd.ab               Same, with split() and strset()
  timezone.ab         Choose a place, date/time to Julian day
  Play.ab             Edit fields, updown buttons, simple bar graph, ini save
  Oracle.ab           Buttons, timer and random
  Monitor Test.ab     Drawing lines and numbers, screen size and DPI
  Font.ab             Show the astrological glyphs of a charset

examples/graphics     Drawing and animation
  GrafixDemo.ab       Timer driven graphics, colors, checkboxes, midi sound
  Happy 2019.ab       Text rendered as a pixel animation
  Planetdance.ab      The planet dance: planets tracing patterns around Earth

examples/horoscope    Working with charts
  Harmonic.ab         Smallest useful example: draw a 2nd harmonic chart
  Radius.ab           Planet positions on a zoomable radius
  Rulers.ab           Dispositor / ruler chains of a chart
  Fixed Stars.ab      Fixed star contacts, rise and set, export
  Midpoints.ab        Midpoints of a chart, also for synastry
  Calendar.ab         Monthly astro calendar with aspects, ingresses, lunations
  Relocate Chart.ab   Relocate a chart to another place

examples/tools        Larger utilities
  Birthdays.ab        Birthday reminder from the database
  DateFind.ab         Find dates when planets are in given sign ranges
  Random.ab           Generate random charts to a database or csv
  Compass.ab          Planet directions (azimuth) drawn on a map
  Browser.ab          Browse a chart database
  Session Manager.ab  Save and restore sets of open charts
  Multi Combine.ab    Composite / combine chart of several people
  Find Return.ab      Find planetary returns
  Library.ab          A library of reusable functions (#name(...) { })

Most examples need Planetdance to run, because they use its charts,
database and ephemeris. To try one: in Planetdance open the AstroBasic
editor, load the .ab file and run it.


License
-------

Copyright Jean Cremers.
