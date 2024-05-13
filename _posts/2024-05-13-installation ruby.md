---
title: "Installation Ruby"
---
# Ruby
Découvrir Ruby en [vingt minutes](https://www.ruby-lang.org/fr/documentation/quickstart/)

Quelques mots sur ruby trouvés sur le site de [ruby-lang.org](https://www.ruby-lang.org/fr/)

Le langage ruby, en terme de syntaxe et de fonctionnalité, a été dès le départ conçu comme un ensemble homogène. Son créateur est le programmeur japonais [Yukihiro « Matz » Matsumoto](http://www.rubyist.net/~matz/). Ce dernier a rassemblé certaines fonctionnalités de ses langages préférés de l’époque (principalement Perl, Smalltalk, Eiffel, Ada et Lisp) afin d’imaginer un nouveau langage qui mêlerait astucieusement programmations impérative et fonctionnelle. À plusieurs reprises, il a déclaré que son but était « d’essayer de rendre Ruby le plus naturel possible, pas nécessairement simple. »

### Installation en utilisant  rbenv
en suivant la doc sur https://linuxize.com/post/how-to-install-ruby-on-ubuntu-20-04/

```
apt install git curl autoconf bison build-essential \
libssl-dev libyaml-dev libreadline6-dev zlib1g-dev \
libncurses5-dev libffi-dev libgdbm6 libgdbm-dev libdb-dev
```

```
curl -fsSL https://github.com/rbenv/rbenv-installer/raw/HEAD/bin/rbenv-installer | bash
```

Misee à jour du PATH

```
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(rbenv init -)"' >> ~/.bashrc
source ~/.bashrc
```

List des installations disponibles :
```
pboizot@sony-vaio:~$ rbenv install -l
3.0.7
3.1.5
3.2.4
3.3.1
jruby-9.4.7.0
mruby-3.3.0
picoruby-3.0.0
truffleruby-24.0.1
truffleruby+graalvm-24.0.1
```

Installation de la version 3.3.1
```
rbenv install 3.3.1
==> Downloading ruby-3.3.1.tar.gz...
-> curl -q -fL -o ruby-3.3.1.tar.gz https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.1.tar.gz
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 21.0M  100 21.0M    0     0  10.7M      0  0:00:01  0:00:01 --:--:-- 10.7M
==> Installing ruby-3.3.1...
-> ./configure "--prefix=$HOME/.rbenv/versions/3.3.1" --enable-shared --with-ext=openssl,psych,+
-> make -j 8
-> make install
==> Installed ruby-3.3.1 to /home/pboizot/.rbenv/versions/3.3.1

NOTE: to activate this Ruby version as the new default, run: rbenv global 3.3.1
```
