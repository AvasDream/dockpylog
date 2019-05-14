## Docker 

DO NOT FORGET RM!!!
```
docker build . -t pyauthlog
# Developement
docker run --rm -it --volume="C:/Users/Tyrell Wellick/git/pyAuthLog:/home/src" pyauthlog /bin/bash
# Production
docker run -it --rm -e DATE="19-04-19"  -v "$(pwd):/home/pyauthlog" pyauthlog

# Delete all images

docker rm $(docker ps -a -q)

docker rmi $(docker images -q)

```

![Example Graph](/examples/19-04-19-country.jpeg)

[Example report](/examples/report-19-04-19.pdf)

## Python 

* Because i get all the filepaths with getcwd script has to be executed from /home/pyauthlog!





## Basemap 


```python
m = Basemap(projection='robin',lon_0=0,resolution='c')
    m.fillcontinents(color='white',lake_color='white')
    m.drawcoastlines()
    # Map (long, lat) to (x, y) for plotting
    for i in lonlat:
        x, y = m(i[0], i[1])
        plt.plot(x, y, 'ro', markersize=3)
    plt.title("Source of login attempts")
    plt.show()
```