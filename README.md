# FFDD Website [![Build Status](https://drone.envs.net/api/badges/freifunk-dresden/dresden.freifunk.net/status.svg)](https://drone.envs.net/freifunk-dresden/dresden.freifunk.net)

[freifunk-dresden.de](https://freifunk-dresden.de/) | [dresden.freifunk.net](http://dresden.freifunk.net/)

## Dependencies
 - Install a javascript runtime, e.g. nodejs
 - Install bundle by running `gem install bundle`
 - Install the dependencies by running `bundle`

```bash
apt install -y git nodejs
```

**ruby 2.2.0**

```bash
curl -L https://get.rvm.io | bash -s stable --ruby=2.2.0
```

**bundler**

```bash
gem install bundler -v 1.17.3
```

## Install
```bash
git clone https://github.com/Freifunk-Dresden/Blog.git /srv/Blog
git clone https://github.com/Freifunk-Dresden/dresden.freifunk.net.git /srv/dresden.freifunk.net
cd /srv/dresden.freifunk.net/
bundle install
```

## Info
On Ubuntu you might need to change the next lines in the 'Rakefile'

*Line 4:* `sh "jekyll build"` to:
```bash
    sh "bundle exec jekyll build"
```
*Line 8:* `sh "jekyll serve"` to:
```bash
    sh "bundle exec jekyll serve"
```

## Building
 - Use `rake build`. This will build the website to the `_site` directory

## Serving (to work locally)
 - Use `rake serve`. This watches files for changes and serves the website on http://0.0.0.0:4000/

## Testing
 - Use `rake test`

State of the current master branch, powered by Travis-CI:
[![Build Status](https://travis-ci.com/Freifunk-Dresden/dresden.freifunk.net.svg?branch=master)](https://travis-ci.com/Freifunk-Dresden/dresden.freifunk.net)

## Deployment
Simply `git push` to the master branch. There's a hook that will automatically deploy it to [dresden.freifunk.net](http://dresden.freifunk.net/)


# Freifunk-Dresden Blog
Blog der Webseite [https://blog.freifunk-dresden.de/](https://blog.freifunk-dresden.de/)

Um einen neuen Beitrag zu erstellen brauchst du keine weitere Software. Das Blog kannst du **direkt im Browser hier auf Github bearbeiten**.  

- Logge dich in deinem Github Account ein

## 1. Klicke einfach oben auf den Ordner [`_posts`](https://github.com/Freifunk-Dresden/freifunk-dresden.github.io/tree/master/_posts) und führe dann folgende Schritte aus:

  - Erstelle eine neue `.md` seite im ordner [`_posts`](https://github.com/Freifunk-Dresden/freifunk-dresden.github.io/tree/master/_posts), drücke dazu rechts oben auf "Create new file":
     ![Create new file](https://raw.githubusercontent.com/Freifunk-Dresden/Blog/master/create_blog_post.png)
     (beim ersten mal wird dabei automatisch eine Kopie dieses Projekts in deinem Github erzeugt, in dem du ab dann arbeitest).
  - Die Benennung der Datei muss dabei mit dem **Datum** (JJJJ-MM-TT) beginnen, gefolgt von einem **Minus**, dann ein rein informativen **Teil der ignoriert wird** und dann **enden auf .md**, z.B. `2019-01-30-beschreibender-ignorierter-teil.md`
  - Der Inhalt der Datei muss anfangen mit den Zeilen:
 ```
 ---
 layout: post
 title: Hier der Titel deiner neuen Seite
 author:
 category: Sonstiges
 ---

 Hier Der Text für deinen neuen Blog Eintrag

 ```
  - Formatierungen können mit den Knöpfen über dem Eingabefeld erstellt werden
  - in dem Reiter "Preview changes" kannst du jederzeit überprüfen, wie dein Post aussehen würde.
  - Author: Das bist du dann sozusagen :)
  - **category: Stelle sicher das die Kategorie auch im Ordner `category` angelegt ist!**
  - optional: Bilder und Media-Files können in den Ordner `downloads` hochgeladen werden.
  - optional: weitere Formatierungen findet man wenn man nach *"markdown cheat sheet"* sucht, z.B. https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

## 2. Wähle dann unten "Propose new file"
## 3. erstelle einen "Pull Request"
Wenn du fertig bist, erstelle einen "Pull Request" mit dem grünen Symbol, dadurch wird ein "Pull Request Issue" erstellt, in dem ein Mitglied des Freifunk Dresden - Blog Projekts deine Änderungen noch einmal anschauen kann und dann freigeben.
