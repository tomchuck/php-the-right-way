# Přispívání do PHP The Right Way

Líbí se Vám [PHP The Right Way](http://phptherightway.com) a chcete se zapojit?
Super! Existuje spousta způsobů jak můžete pomoci.

Věnujte prosím chvíli prostudování tohoto dokumentu, aby byl proces poskztování
příspěvků pro všechny zúčastněné snadný a efektivní.

Dodržováním těchto pokynů dáváte najevo, že respektujete čas vývojářů, kteří
tento open source projekt spravují a vyvíjejí. Na oplátku by vám měli tento
respekt oplatit tím, že se budou zabývat vaším problémem nebo posuzovat opravy
a funkce.

## Použití nástroje _Issue tracker_ pro sledování problémů

[Issue tracker](https://github.com/tomchuck/php-the-right-way/issues) je
preferovaným kanálem pro změny: pravopisné chyby, změny formulací, nové
informace obsahu a obecně [zasílání pull requestů](#pull-requests), ale prosím
respektujte následující omezení:

* Prosím **nepoužívejte** _Issue tracker_ pro osobní žádosti o podporu (použijte
  [Stack Overflow](http://stackoverflow.com/questions/tagged/php) nebo IRC).

* Prosím **nevykolujte** ani netrollujte. Udržujte diskusi k tématu a respektujte
  názory ostatních.


<a name="pull-requests"></a>
## Pull Requesty

Pull requesty jsou skvělým způsobem, jak přidávat nový obsah do PHP The Right Way,
stejně jako aktualizovat případné problémy s prohlížeči nebo jiné změny stylu.
Přijímají se prakticky jakékoli změny, pokud jsou považovány za konstruktivní.

Dodržování následujícího postupu je nejlepší způsob, jak do projektu zařadit
svou práci:

1. [Forkněte](http://help.github.com/fork-a-repo/) projekt, naclonujte svůj fork,
   a nakofigurujte remoty:

   ```bash
   # Clone your fork of the repo into the current directory
   git clone https://github.com/<your-username>/php-the-right-way.git
   # Navigate to the newly cloned directory
   cd php-the-right-way
   # Assign the original repo to a remote called "upstream"
   git remote add upstream https://github.com/codeguy/php-the-right-way.git
   ```

2. Pokud jste klonovali před nějakou dobou, získejte nejnovější změny z
   upstreamu:

   ```bash
   git checkout gh-pages
   git pull upstream gh-pages
   ```

3. Vytvořte novou tematickou větev (mimo hlavní vývojovou větev projektu),
   která bude obsahovat vaši změnu nebo opravu:

   ```bash
   git checkout -b <topic-branch-name>
   ```

4. Nainstalujte [Jekyll](https://github.com/jekyll/jekyll/) gem a závislosti pro lokální zobrazení:

    ```bash
    # Install the needed gems through Bundler
    bundle install --path vendor/bundle
    # Run the local server
    bundle exec jekyll serve
    ```

5. Commit změn provádějte v logických celcích. Prosím dodržujte tyto pokyny [git commit
   message guidelines](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
   jinak je nepravděpodobné, že bude váš obsah začleněn do hlavního projektu.
   Před zveřejněním commitů použijte [interaktivní rebase](https://help.github.com/articles/about-git-rebase/)
   systému Git k jejich pročištění.

6. Proveďte lokální merge (nebo rebase) vývojové větve upstream do tématické větve:

   ```bash
   git pull [--rebase] upstream gh-pages
   ```

7. Pushněte svoji tématickou větev dosvého forku:

   ```bash
   git push origin <topic-branch-name>
   ```

8. [Otevřete Pull Request](https://help.github.com/articles/using-pull-requests/)
    s jasným názvem a popisem.


## Dohoda o přispívání a používání

Odesláním pull requestu do tohoto repozitáře souhlasíte s tím, že vlastníkům projektu umožníte
licencovat Vaši práci pod podmínek [Creative Commons Attribution-NonCommercial-ShareAlike
3.0 Unported License](http://creativecommons.org/licenses/by-nc-sa/3.0/).

Stejný obsah a licence budou použity pro všechny publikace PHP The Right Way,
včetně - ale nejen pro:

* [phptherightway.com](http://phptherightway.com)
* Překlady phptherightway.com
* [LeanPub: PHP The Right Way](https://leanpub.com/phptherightway/)
* Překlady "LeanPub: PHP The Right Way"

Veškerý obsah je nyní kompletně zdarma a vždy bude.

## Průvodce stylem přispěvatele

1. Používejte americký anglický pravopis (*primární jen English repozitář*)
2. Pro odsazení textu používejte čtyři (4) mezery; nepoužívejte tabulátory
3. Zalamujte veškerý text na maximálních 120 znaků na řádek
4. Ukázky kódu by měly odpovídat standardu PSR-1 nebo vyššímu
5. Pro veškerý obsah používejte [GitHub Flavored Markdown](https://github.github.com/gfm/)
6. Při odkazování na externí webové stránky, jako je například příručka [php.net](http://php.net/urlhowto.php),
   používejte jazykově agnostické URL adresy
