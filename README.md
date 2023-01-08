# Semantic Directory Naming Scheme (semdir)

_SemDir_ is a naming scheme that details how files and folders should be named, for a drive or directory containing films, series, or other video media.

**Version 0.1.0** | [Latest Version](https://github.com/darccyy/semdir#semantic-directory-naming-scheme-semdir)

# Contents

- [Semantic Directory Naming Scheme (semdir)](#semantic-directory-naming-scheme-semdir)
- [Contents](#contents)
- [File and Folder Types](#file-and-folder-types)
  - [All Files and Folders](#all-files-and-folders)
    - [File Extensions](#file-extensions)
  - [Film Files](#film-files)
  - [Series Folders](#series-folders)
    - [Season Folders](#season-folders)
    - [Episode Files](#episode-files)
  - [Categories](#categories)
- [Episode Code](#episode-code)
  - [Pilot Episodes](#pilot-episodes)
- [Minor Words](#minor-words)
  - [Initial Article](#initial-article)
- [Other Folders](#other-folders)
  - [Meta Files](#meta-files)
  - [Temporary Files](#temporary-files)

# File and Folder Types

> _Note:_ in this file, paths starting with `~/` are located in the root directory, in which this scheme is enforced.

## All Files and Folders

These rules apply to all types of file and folder.

All file and folder names:

1. _Must_ capitalize the first letter of every major word
   - See [Minor Words](#minor-words) for exceptions
   - _Eg._ `The Hunger Games`
2. _Must_ not contain spaces - Use periods instead
   - _Eg._ `The.Hunger.Games`
3. _Must_ only contain ASCII characters
   - Non-English text _should_ be transliterated or translated (either option is accepted)
   - _Eg._
     - `La Vita e Bella` or `Life Is Beautiful` (originally `La vita è bella`)
       - In this example, the first word is `La`, however it is not necessarily considered an [Initial Article](#initial-article), and might not necessarily be displaced
     - `Kalina krasnaya` or `The Red Snowball Tree` (originally `Калина красная`)
4. _Must **not**_ include properties such as resolution, download source, ect.
5. _Should_ include `{aka}` before an alias of the title, if relevent

### File Extensions

> _Note:_ File extensions for file names have been omitted for most examples in this file

Video files _should_ use any widely-accepted format, such as `.mp4`, `.avi`, or `.mkv`; however, standard video formats are preferred, for compatibility.

## Film Files

File names for film:

1. _Must **not**_ begin with an [Initial Article](#initial-article), such as `the`
   - The article _must_ be appended, lowercase, to end of name, separated by comma
   - _Eg._ `Hunger.Games,the`
   - A period _must **not**_ follow the final comma, such as `Hunger.Games,.the`
2. _Must_ include the date, after the title, in square brackets
   - Date _must **not**_ be shortened
   - _Eg._ `Hunger.Games,the[2012]`
3. _Must_ include part or disc number, if relevant, after title and date, in curly braces (`{` and `}`)
   - This does **not** include films in a series or franchise, such as a sequel
   - _Eg._ `Hunger.Games,the[2012]{1}` and `Hunger.Games,the[2012]{2}`, for discs 1 and 2
4. _Must_ include the series (sequel) number, if relevant, after the title
   - The subtitle _should_ be included, if relevant, after the series number
       <!-- - Include leading zeros -->
   - No punctuation should be included between the series number and subtitle
   - _Eg._ `Hunger.Games,the[2012]`
     - This is accepted if it is the only film of the series that is in the directory
   - _Eg._ `Hunger.Games,the.1[2012]` and `Hunger.Games,the.2.Catching.Fire[2013]`
     - For two films in the series. Note that the `.1` is included in the first name, as would the subtitle, if relevant
     - **NOT** `Hunger.Games,the.2.-.Catching.Fire[2013]` or `Hunger.Games,the.Catching.Fire[2013]`
   - The number can be written in _roman numerals_, if necessary, after the series number, surrounded by round brackets (`(` and `)`)
     - _Eg._ `Star.Wars.4(IV).A.New.Hope[1977]`
       <!-- - If the first in a film series using roman numerals -->

## Series Folders

Series folders should contain [Season Folders](#season-folders).

Miscellaneous files, such as Special Features, are counted as [Episode Files](#episode-files), but located in the Series Folder directly.

Series folders _must **not**_ include the date, as that is included in each [Season Folder](#season-folders).

Folder names for a series:

1. _Must **not**_ begin with an [Initial Article](#initial-article), such as `the`
   - Append, lowercase, to end of name, separated by comma
   - _Eg._ `Boys,the`
   - A period _must **not**_ follow the final comma, such as `Boys,.the`

### Season Folders

Folder names for a series season:

1. _Must_ begin with `Season.`, followed by the season number
2. _Must_ include the date, after the season number, in square brackets
   - Date _must_ be year of first airing, unless year of last airing is 2 calendar years greater than first airing, where it _must_ include both, separated by a dash
   - Dates _must **not**_ be shortened
   - _Eg._
     - `Season.1[2009]` - Aired only in `2009`
     - `Season.2[2010]` - Aired from `2010` to `2011` - 1 calendar year difference
     - `Season.3[2012-2014]` - Aired from `2012` to `2014` - 2 calendar year difference
       - **NOT** `Season.3[2012-14]`

### Episode Files

All Episode Files _must_ be located in the [Season Folder](#season-folders) corresponding to it's [Episode Code](#episode-code).
This includes ['Pilot' episodes](#pilot-episodes).

Miscellaneous files, such as Special Features, are counted as [Episode Files](#episode-files), but located in the Series Folder directly.

File names for a series episode:

1. _Must_ consist of: The series title, [Episode Code](#episode-code), and episode title, in that order, all separated by periods
   - _Eg._ `Modern.Family.S01E07.En.Garde`
2. Series and episode titles _must **not**_ displace an [Initial Article](#initial-article), such as `the`
   - _Eg._ `The.Boys.S02E01.The.Big.Ride`
   - This is different from [series](#series-folders) and [films](#film-files)
3. _Must_ include part or disc number, if relevant, after title, in curly braces (`{` and `}`)
   - Episodes might not necessarily have the same title
   - _Eg._ `Adventure.Time.S02E24.Mortal.Folly{1}` and `Adventure.Time.S02E24.Mortal.Recoil{2}`, for parts 1 and 2 of a 2-episode plot

## Categories

Categories are folders which can include [films](#film-files) and [series](#series-folders), but not standalone (orphan) [Season Folders](#season-folders) or [Episode Files](#episode-files).

Categories can contain any [film](#film-files) or [series](#series-folders) deemed to be related (subjective).

For franchise categories, the name of a franchise (as well as any joining [Minor Words](#minor-words)) can optionally be excluded from film, series, or episode titles, if the file name is still relevant.

A category name _must_ begin with an underscore (`_`), to rank higher alphabetically.

- A category name may begin with an two underscores (`__`), to rank before any other category.

Shortcuts to other files or folders in the same drive may be included.

Categories can be nested, but this is not recommended.

- _Eg._ `~/_Scooby.Doo` - Contains the films `Zombie.Island[1998]` and `Witch's.Ghost[1999]`, and series `What's.New`, with an episode named `What's.New.S01E04.Big.Scare.in.the.Big.Easy` in `Season.1[2002]`

# Episode Code

Episode codes are unique numbers for an episode.

_Must_ follow the format `SxxExx`, or `SxxExxx` if the number of episodes in the season exceeds 99.

`Exx` or `Exxx` _should_ be used instead of `SxxExx` or `SxxExxx` respectively, if the series is not split into [seasons](#season-folders).

Both the Season number and Episode number _must_ include leading zeros.

All files in a folder _must_ use the same type of episode code.

| Code Type | Use                       | Code Length | _Example 1_ | _Example 2_ |
| --------- | ------------------------- | ----------- | ----------- | ----------- |
| `SxxExx`  | Default type              | 6           | `S01E02`    | `S12E13`    |
| `SxxExxx` | If episodes > 99          | 7           | `S03E004`   | `S19E123`   |
| `Exx`     | No seasons                | 3           | `E02`       | `E13`       |
| `Exxx`    | No seasons, episodes > 99 | 4           | `E05`       | `E572`      |

## Pilot Episodes

<!-- TODO Reword this -->

'Pilot' episodes _should_ be located:

- In the `Season.1` folder, if there is only 1 Pilot, with [Episode Code](#episode-code): `S01E00` (or `S01E000`)
- Or in the `Season.0` (Pilot season) folder, with [Episode Codes](#episode-code): `S00E01`, `S00E02`, ect. (or `S00Exxx`)
- Or in the [Series Folder](#series-folders) directly, with [Episode Code](#episode-code): `E00` (or `E000`)

# Minor Words

Minor words are words that _must_ be lowercase in a film, series, or episode title, unless the first word in a title.

- _Eg._ `Scooby.Doo.and.the.Witch's.Ghost[1999]`

This includes prepositions, conjunctions, and articles.
A minor word _should_ be no longer than 4 letters.

- _Eg._ '_the_', '_a_', '_and_', '_or_', '_for_', '_of_', '_from_', '_to_', ect.

Classification is case-by-case.

## Initial Article

Initial articles are the words `the` and `a` at the beginning of an original title.

The article _must_ be appended, lowercase, to end of name, separated by comma, when required.

- _Eg._ `Hunger.Games,the`

A period _must **not**_ follow the final comma, such as `Hunger.Games,.the`.

# Other Folders

## Meta Files

_Meta files_ are files that relate to the root directories contents, but are not intended for user interaction.

These files _should_ be located in `~/.meta`, which may be hidden.

- _Eg._ `~/.meta/tree.txt` contains a list of all files, in tree form.
- _Eg._ `~/.meta/semdir.md` is a duplicate of this file.

## Temporary Files

_Temporary files_ are files or folders that are temporary. This includes current downloads, or redundant folders that will be removed.

These files _should_ be located in `~/.temp`, which may be hidden.

Temporary files _should_ be surrounded by curly braces (`{` and `}`)

- _Eg._ A folder named `{Hunger.Games,the[2012]}`, in the directory `~/.temp`, which contains `Hunger.Games,the[2012].mp4`. The video file will be moved into `~/` when the download has finished, and the folder will be deleted.
