# cgit docker container
![cgit.](https://github.com/oemunoz/cgit/raw/master/images/cgit.png)

Cgit is an attempt to create a fast web interface for the git version control system, using a built in cache to decrease pressure on the git server.
https://git.zx2c4.com/cgit/
## To run the image:

## Mounting the git repository volume

Using your own git repository (make backup of your original data before to load this docker):

~~~~bash
docker run -d -p 80:80 -v $PWD/gitrepo:/mnt/git oems/cgit
~~~~

![cgit_shot1.](https://github.com/oemunoz/cgit/raw/master/images/cgit_shot1.png)

## Build your own:

Modify the mysql_wikkawiki.sql with your own user and database definitions and build the image:

~~~~bash
git clone git@github.com:oemunoz/cgit.git cgit
cd cgit
docker build -t "cgit" .
~~~~

## History

 - 160705: Basic Initial Version.
 - 160706: Work out of the box.

## Credits

https://git.zx2c4.com/cgit/about/

## License

GNU General Public License
