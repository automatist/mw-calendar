May 2020
==========

* Replace [PrefixSearch](https://gerrit.wikimedia.org/g/mediawiki/core/+/master/includes/search/PrefixSearch.php), deprecated in mw 1.27 with [SearchEngine::defaultPrefixSearch](https://doc.wikimedia.org/mediawiki-core/master/php/classSearchEngine.html). Usage hint taken from [here](https://doc.wikimedia.org/mediawiki-core/master/php/SpecialPage_8php_source.html).
 

```php
        $searchEngine = MediaWikiServices::getInstance()->newSearchEngine();
        $pages = $searchEngine->defaultPrefixSearch( $search );
        foreach($pages as $page) {
            $this->addArticle($month, $day, $year, strval($page));
        }
```

TODO: check for more deprecated functions!!!


Febrary 2021
=============

* Replaced deprecated class constructors (with _ _ construct)
* Replaced each for foreach
* Commented out (thus disabling) the Common checkForMagicWord function -- not sure how to replace getVariableValue. There is an "expandMagicVariable" method in Parser, but it's private. Disabling the code has no visible effect on the usage of calendar I've tested (I don't recall any use of magic words in practice).


