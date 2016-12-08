# [cgit docker container](https://github.com/oemunoz/cgit)
![cgit.](https://github.com/oemunoz/cgit/raw/master/images/cgit.png)

CgIt is a **fast web interface** for the git version control system, using a built in cache to decrease pressure on the git server.
https://git.zx2c4.com/cgit/

## To run the image:

This is a basic implementation and gonna stay on this way, works very well out the box. If you look for aditional features look on my other dockers.

### How to use it?

#### Mounting the git repository volume
The basic use of the docker, replace the gitrepo with you directory.

```bash
docker run -d -p 80:80 -v $PWD/gitrepo:/mnt/git oems/cgit
```

Using your own git repository (make backup of your original data before to load this docker):

```bash
docker run -d -p 80:80 -v $PWD/gitrepo:/mnt/git oems/cgit
```

![cgit_shot1.](https://github.com/oemunoz/cgit/raw/master/images/cgit_shot1.png)

## Build your own:

Modify the mysql_wikkawiki.sql with your own user and database definitions and build the image:

```bash
git clone git@github.com:oemunoz/cgit.git cgit
cd cgit
docker build -t "cgit" .
```

## About this implementation:
This implementation downloads the code from the main page and compile it, this is not a installation from the repos.

## Features
- highlight
- subdirectory search
- Readme parse. (About)
- Check with md5sum the tar.gz before compile it.

## History
I gonna to leave this docker only with the Upgrades and basic options and changes, there is some people using it.

 - 161207: Update the Docker file to the ADD for download the code.
 - 160706: Work out of the box.
 - 160705: Basic Initial Version.

## Credits
To the real coders!!!
https://git.zx2c4.com/cgit/about/

## License

GNU General Public License
