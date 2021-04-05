
 ![alt text](https://i.imgur.com/vbH9sWZ.png)


In order to install the theme and add it to your decorations do the following:

First make sure you have [`extra-cmake-modules`](https://github.com/KDE/extra-cmake-modules) installed:

```
git clone https://github.com/KDE/extra-cmake-modules.git
cd extra-cmake-modules
mkdir build && cd build    
cmake ..
make && sudo make install
```

Then install with:

``` shell
git clone https://github.com/jomada/SierraBreeze
cd SierraBreeze
mkdir build
cd build
cmake .. -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Release -DKDE_INSTALL_LIBDIR=lib -DBUILD_TESTING=OFF -DKDE_INSTALL_USE_QT_SYS_PATHS=ON
sudo make install
```
To avoid logging out, issue
``` shell
kwin_x11 --replace &
```
That is it! Your new decoration theme should appear in
*Settings &rarr; Application Style &rarr; Window Decorations*.

## Acknowledgments:
- The authors of Breeze window decorations Martin Gräßlin and Hugo Pereira Da Costa
- Andrey Orst, the author of Breezemite Aurorae window decoration
https://github.com/andreyorst/Breezemite
- Chris Holland for his blog about patching Breeze decorations
https://zren.github.io/projects/2017/07/08/patching-breeze-window-decorations.html
