# Cowyo...

_...is the Collection of Online Words You Open._

This tool is supposed to make sharing online notes and lists fast and easy. To jot a note, simply load the page at [`/`](http://cowyo.com/) and write. The url will redirect to an easy-to-remember name that you can use to reload the page at anytime, anywhere. (You can use any url you want too: [`/AnythingYouWant`](http://cowyo.com/AnythingYouWant)). No need to press save, it will automatically save when you stop writing.

You can also write your notes in [Markdown](https://daringfireball.net/projects/markdown/) and then render your page by adding `/view`. For example, the page `/about` is rendered at [`/about/view`](/about/view).

If you are writing a list and you want to tick off things really easily, just add `/list`. For example, after editing [`/grocery`](http://cowyo.com/grocery), goto [`/grocery/list`](http://cowyo.com/grocery/list). In this page, whatever you click on will be striked through and moved to the end. This is helpful if you write a grocery list and then want to easily delete things from it.

Math is supported using [Katex](https://github.com/Khan/KaTeX). 

Be cautious about writing sensitive information in the notes as anyone with the URL has access to it. For more information, or if you'd like to edit the code, [use the github](https://github.com/schollz/cowyo).

**Powered by Raspberry Pi and Go** ![Raspberry Pi](http://cowyo.com/static/img/raspberrypi.png) ![Go Mascot](http://cowyo.com/static/img/gomascot.png)

# Install

`go install github.com/schollz/cowyo`

## Production server

I recommend using `NGINX` as middleware, as it will do caching of the static files for you. There is an example `NGINX` block in `install/`.

# Usage

```
$ cowyo --help
cowyo: a websocket notepad
run this to start the server and then visit localhost at the port you specify
(see parameters).
Example: 'cowyo localhost'
Example: 'cowyo -p :8080 localhost'
Example: 'cowyo -db /var/lib/cowyo/db.bolt localhost'
Example: 'cowyo -p :8080 -crt ssl/server.crt -key ssl/server.key localhost'
Options:
  -crt string
        location of ssl crt
  -db string
        location of database file (default "/home/mu/cowyo/data.db")
  -httptest.serve string
        if non-empty, httptest.NewServer serves on this address and blocks
  -key string
        location of ssl key
  -p string
        port to bind (default ":12312")```
```
