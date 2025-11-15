# hot diva 2004

a random writing prompt generator webpage  with a catch: it's powered by [hotdiva2000](https://github.com/charmbracelet/hotdiva2000)!

the site is compiled from the **build.sh** script, which will randomly generate 100 strings with hotdiva2000, then create or update an index.html file that can be served anywhere.

styling can be customized through the **main.css** file.

the project name is "hotdiva2004" because 2004 is my birth year :)

## live demo

```
https://prompts.4-walls.net/hotdiva2004/
```

the prompts can be updated by setting the script to run and compile the page via a cron job, such as the one below, which updates it every hour:

```bash
0 * * * * cd /var/www/hotdiva2004 && /var/www/hotdiva2004/build.sh
```

## dependencies

- go 1.21+
- [hotdiva2000](https://github.com/charmbracelet/hotdiva2000)
- paste
- sed

### building hotdiva2000 from source

the hotdiva2000 docs are a bit sparse, so if you're unfamiliar with go and want to install this, here's a quick guide:

- git clone the hotdiva2000 repo
- from the project's root, ``cd`` to ``cmd/hotdiva2000``
- build the program with ``go build main.go``
- copy the new ``main`` executable to ``/usr/local/bin/hotdiva2000``
