## Bienvenido a weki APPSEC 

Podras poner todo lo que necesites (Herramientas , codigo , comandos , enlaces)

You can use the [editor on GitHub](https://github.com/SEC-ERICK/SEC-ERICK/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.


### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for


```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```
### Syntax SCRIPT PRUEBAS

```markdown


#!/bin/bash
for target in $(cat url)
do
echo " OPENPAY      --      AUTOMATIC  PENTESTING " 

echo " ###########################################"
echo " ###           SN1PER                     ##"
echo " ###########################################"  
echo ""
echo ""
echo ""
echo ""
echo ""
echo ""

sniper -t $target
# NMAP 

      # CREAR NUEVOS DIRECTORIOS PARA LOS RESULTADOS
       ## mkdir -p "$FILE_PATH/IG"
       ## mkdir -p "$FILE_PATH/IG/NMAP"
        echo 'NMAP  is scanning...'
echo " ###########################################"
echo " ###           NMAP                     ##"
echo " ###########################################"
        # syn-scan
        echo 'start syn-scan with syn-probe...'
       ## nmap -vvv -oA "$FILE_PATH/IG/NMAP/$SCRIPT_SYN" -PE -PS80,443,22,25,110,445 -PU -PP -PA80,4$
echo "METODOS DISPONIBLES"    
    
nmap -p80,443 --script http-methods $target
nmap -A -Pn -n -T4 -sV $target
nmap -A -Pn -n -T4 -sV -O -v $target
nmap $target
nmap -sV -O -v  $target

# AMASS 
echo " ###########################################"
echo " ###           AMASS                     ##"
echo " ###########################################"

echo "AMASS   is scanning"

amass enum -passive -d  $target -src
amass enum -asn 28000 -d $target
amass enum -brute -src -d $target -demo
amass db -d $target -enum 1 -summary
amass intel -d $target -whois

# THE HARVESTER 
echo " ###########################################"
echo " ###           THE HARVESTER             ##"
echo " ###########################################"

theharvester -d $target -b all 

# NIKTO
echo " ###########################################"
echo " ###           NIKTO                      ##"
echo " ###########################################"

nikto -h $target -Display 1234EP 
nikto -h $target -Tuning 12348abde -mutate 3456 -ssl -list-plugins

# WHATWEB 
echo " ###########################################"
echo " ###           WHATWEB                    ##"
echo " ###########################################"
whatweb -v  $target -a 3

# SSLSCAN  
echo " ###########################################"
echo " ###           SSLSCAN                    ##"
echo " ###########################################"
##sslscan $target

# SQLMAP 
echo " ###########################################"
echo " ###           SQLMAP                     ##"
echo " ###########################################"

##sqlmap -u $target  --tables --dbs --dump --current-db --current-user --privileges

# WAFW00F
echo " ###########################################"
echo " ###           WAFW00F                    ##"
echo " ###########################################"
wafw00f $target

# DIRB
echo " ###########################################"
echo " ###           DIRB                    ##"
echo " ###########################################"
 dirb https://$target -w

# Hakrawler 
echo " ###########################################"
echo " ###           Hakrawler                   ##"
echo " ###########################################"

~/go/bin/hakrawler --url $target  -depth 4

# XSStrike
echo " ###########################################"
echo " ###           XSStrike                   ##"
echo " ###########################################"

 xsstrike -u $target  --blind --console-log-level INFO --path

# CURL 
echo " ###########################################"
echo " ###           CURL                   ##"
echo " ###########################################"

curl -v https://$target

# WPSCAN 
echo " ###########################################"
echo " ###           WPSCAN                  ##"
echo " ###########################################"

wpscan --url $target -e ap at 
wpscan --url $target -e u
done

```
## Herramientas
Listado de herramientas que necesitas
### OWASP ZAP
OWASP ZAP es un escáner de seguridad web de código abierto. Pretende ser utilizado como una aplicación de seguridad y como una herramienta profesional para pruebas de penetración. Es uno de los proyectos más activos de OWASP. 
[Descargar](https://www.zaproxy.org/download/). 


### Docker

Docker es un proyecto de código abierto que automatiza el despliegue de aplicaciones dentro de contenedores de software, proporcionando una capa adicional de abstracción y automatización de virtualización de aplicaciones en múltiples sistemas operativos
[Descargar](https://www.docker.com/products/docker-desktop). 

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

---
layout: default
---

Text can be **bold**, _italic_, ~~strikethrough~~ or `keyword`.

[Link to another page](./another-page.html).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>
