# Rocksmith 2014 Tab Converter

#### Summary
Exports Rocksmith 2014 arrangements to Guitar Pro 6 (.gpx). It's a command line utility, you have to specify the Rocksmith archive (.psarc) you wish to process and an output directory for the tabs. Optionally, you can select individual songs from the archive and individual arrangements. By default, all selected arrangements are put into a single file, but you can tell the program to create a separate file for each arrangement.

Basic use:

`RocksmithToTab.exe -p \Path\To\Rocksmith2014\songs.psarc -o rocksmith_tabs`

#### Command line options
```
Usage: RocksmithToTab -p archive.psarc [-a bass,lead] [-s song1,song2]

  -p, --psarc     Required. PSARC song archive to open.

  -l, --list      List songs contained in the archive. No conversions are 
                  performed.

  -s, --songs     Comma-separated list of tracks to include. (default: all)

  -a, --arr       Comma-separated list of arrangements to include. (default: 
                  all)

  -t, --split     Create a separate file for each arrangement.

  -d, --diff      (Default: 255) Difficulty level. (default: max)

  -o, --outdir    Path to the directory where tabs should be created. (default:
                  current work dir)

  -f, --format    (Default: gpx) File output format, currently either 'gpx' or 
                  'gpif'. (default: gpx)

  --help          Display this help screen.
```

#### Caveats
* Bends are not yet implemented.
* Sustains are not yet handled.
* Some slides do not work correctly.
* The rhythm detection occasionally screws up, particularly in fast and "sloppy" solos.

#### Acknowledgements
Many thanks to the people at www.rscustom.net for creating the Rocksmith Custom Toolkit, without which this exporter would not have been possible. Likewise, I'd probably never have started this project if I didn't have the code from the [RSTabExplorer](https://github.com/andulv/RSTabExplorer) project as a starting point!