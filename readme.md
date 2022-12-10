# Serve locally
```
export JEKYLL_VERSION=3.8
```
```
docker run --rm \
  --volume="$PWD:/srv/jekyll:Z" \
  --publish="[::1]:4000:4000" \
  jekyll/jekyll:$JEKYLL_VERSION \
  jekyll serve
```

# Build
```
docker run --rm \
  --volume="$PWD:/srv/jekyll:Z" \
  -it jekyll/jekyll:$JEKYLL_VERSION \
  jekyll build
```