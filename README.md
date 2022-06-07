# git-activity

A custom git command to display an activity graph (like the contribution graph on GitHub) for the current git repository and branch. To add this custom git command to git, just place the file in a folder that's in your path (a.k.a `PATH`). You can [setup `git-activity` as custom command](https://github.com/aaossa/git-activity/wiki/Setup-'git-activity'-as-custom-command).

### Usage

```bash
# Display activity for this branch
$ git activity -h
Usage: git-activity [-h] [-n] [-s style]

Display an activity graph (like the contribution graph on GitHub) for the
current git repository and branch

Available options:

-h, --help      Print this help and exit
-n, --no-space  Remove spaces between week columns
-s, --style     Sets style of the graph: square (default), block, or plus
```

The output of the command displays a colored graph similar to the one that you can find in any GitHub profile webpage:

```bash
# And... a sample output (of course, does not contain colors)
$ git activity
        Jun     Jul     Aug       Sep     Oct     Nov       Dec     Jan       Feb     Mar     Apr     May     
    ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ 
Mon ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■
    ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ 
Wed ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ 
    ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■
Fri ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■
    ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■ ■

 Less ■ ■ ■ ■ ■ More
```

![image](https://user-images.githubusercontent.com/10425834/170083409-9ac54a18-8de5-4a7d-8338-375d285e5547.png)

There are also a couple of different styles available (square, block, and plus), and spacing between columns can be disabled:

```bash
# Another example to highlay some of the available options
$ git activity --no-space --style block
      Jun Jul Aug  Sep Oct Nov  Dec Jan  Feb Mar Apr May 
    █████████████████████████████████████████████████████
Mon █████████████████████████████████████████████████████
    █████████████████████████████████████████████████████
Wed ████████████████████████████████████████████████████
    ████████████████████████████████████████████████████
Fri ████████████████████████████████████████████████████
    ████████████████████████████████████████████████████

 Less █ █ █ █ █ More
```

![image](https://user-images.githubusercontent.com/10425834/170083883-6145a11f-b6d8-490e-a751-45c2d6552698.png)

### Run On Mac

Just need install `coreutils`, execute cammond `brew install coreutils` if you had brew.

### License

This software is released under the [MIT License](https://opensource.org/licenses/MIT)
