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
