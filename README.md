# agile-planning

(Marp-Next) HowTo Use

Pull the needed docker image (if you don't want Node installed locally)
(https://hub.docker.com/r/marpteam/marp-cli/)
```
docker pull marpteam/marp-cli
```

Use as a local webserver
```
docker run --rm --init -v $PWD:/home/marp/app -e LANG=$LANG -p 8080:8080 -p 37717:37717 marpteam/marp-cli -s .
```

Convert in html
```
docker run -u "node" --rm --init -v $PWD:/home/marp/app/ -e LANG=$LANG -p 8080:8080 -p 37717:37717 marpteam/marp-cli agile-planning.md --html
```

Convert in pdf
```
docker run -u "node" --rm --init -v $PWD:/home/marp/app/ -e LANG=$LANG -p 8080:8080 -p 37717:37717 marpteam/marp-cli agile-planning.md --pdf --allow-local-files
```
