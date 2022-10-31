# My build of slstatus

---

## Preview:

![Preview](preview.png)

---

## Dependencies:

+ Volume Meter requires `pamixer`
+ Updates Counter requires `checkupdates` included in `pacman-contrib`

---

## Updates Counter: 

slstatus does not directly run `checkupdates` as that would be ineffective. Instead, it runs `cat` on `$XDG_CACHE_HOME/updates.txt` and pipes it to `wc -l`.

So what I do is I have my **Xinitrc** run `checkupdates > $XDG_CACHE_HOME/updates.txt &` on login. This way you are not allways querying for updates.

---

## Contact

- [Github](https://github.com/FawkesOficial)
- [Twitter](https://twitter.com/FawkesOficial)
