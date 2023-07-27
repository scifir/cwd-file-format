# CWD file format
**Version:** 1.0.0-beta

**Created Words Document**, of acronym **CWD**, is an XML file format that allows to create files of new words. A new word is any new word created not included in the official dictionary of the language, but useful for some, or a big amount, of purposes. Also, CWD allows to create new bywords and new prefixes.

### Invented words, glossaries and invented glossaries

CWD allows to create **creawords** or **created words**, which are defined as words created expressly by the mind, not naturally as common words, and then not registered on the official dictionary of the language of which the invented word now belongs.

By contrast, a **natural word** is a word that naturally is present on the human language.

A **glossary** is defined, in english, in his official dictionary, as a catalogue of words of the same discipline.

A **creaglossary** or **created glossary** is defined here, as part of CWD, as a glossary invented expressly by humans, by thinking each word, instead of being a natural one.

### Rules for creating words

The rules, which are mandatory to follow in order to don't break the language, for creating new words are the following:

- The word can’t be **already defined** inside the official dictionary or any important glossary being massively used.
- The **definition** can’t be another word, as synonym, it must be explained.

### Guidelines for creating words

The guidelines for creating new words, which are not mandatory but highly recommend to respect, are the following:

- The word shouldn’t be created if the author doesn’t **knows deeply** the language of the word. If it’s needed to translate a creaword of another language it’s better to search for a translator that is expert on the required language rather than trying to create the new word alone.
- The word shouldn’t have **synonyms** or **antonyms**, unless it’s strictly necessary.

### Properties of CWD words

The words created with CWD have the following properties:

- **name:** The word.
- **type:** If the word is a sustantive, adjective, verb or adverb.
- **singular:** The singular form of the word. It’s specified as the name. The singular form has a masculine and a femenine form sometimes, sometimes is has only one form.
- **plural:** The plural form of the word. The plural form can also have a masculine and a femenine form.
- **description:** The meaning of the word.
- **etymology:** The words that form the word, if the word has an etymology.
- **synonym:** If there’re, the words which are synonyms of this word.
- **antonym:** If there’re, the words which are antonyms of this word.
- **parent:** If there’s, a word that’s a parent of this word, and then this word pertains to an ontology of words.

### Properties of CWD prefixes

The prefixes created with CWD have the following properties:

- **name:** The prefix.
- **description:** What the prefix adds as a meaning to a word.
- **etymology:** The words from which the prefix has been created, if there are.

### Properties of CWD bywords

The bywords created with CWD have the following properties:

- **name:** The byword.
- **description:** What the byword means.
- **plural:** The plural form of the byword.

## XML elements

The XML elements for cwd files are the following:

| XML element | Use | Description
| -------- | ---------| ----------------------------|
| \<dictionary\> | Required, top level | Top-level element to create cwd words inside |
| \<word\> | Optional, any number | Creates a new word |
| \<prefix\> | Optional, any number | Creates a new prefix |
| \<byword\> | Optional, any number | Creates a new byword |

### \<word\>

A word is created inside a cwd file as follows:

```xml
<word name="worda" type="sustantive">
	<en singular="worda" plural="wordsa" etymology="word,a">This is an example word.</en>
	<es singular="palabraa" plural="palabrasa" etymology="palabra,a">Ésta es una palabra de ejemplo.</es>
</word>
```

The tags for each definition, in each language, have as name the acronym of that language as specified in the ISO of Languages called **ISO 639**. It’s used the two letter code **ISO 639-1**.

### \<byword\>

A byword is like a word, but it's composed of two or more different words, and has a special meaning compared to the meaning of the two words without the definition of the byword.

An example of a byword is the following:

```xml
<byword name="rolics researcher">
	<en name="rolics researcher" plural="rolics researchers">Synonym of rolic.</en>
	<es name="investigador de rólica" plural="investigadores de rólica">Sinónimo de róltico.</es>
</byword>
```

### \<prefix\>

A prefix is used to give meaning to a word related to some central idea. It means that the word is related to that meaning in some manner.

An example of a prefix is the following:

```xml
<prefix name="rol-">
	<en name="rol-">The word it precedes is related to rolics.</en>
	<es name="rol-">La palabra a la que precede está relacionada con la rólica.</es>
</prefix>
```

### \<category\>

A category is used to group words, bywords and prefixes. It's useful to have all related definitions grouped inside a central idea. Then, it can be used to display all the words, bywords and prefixes by category inside a document.

An example of a category is the following:

```xml
<category name="rólica" canonical_name="rolica">
...
</category>
```

Inside \<category\> any number of xml elements \<word\>, \<byword\> and \<prefix\> can be added.

## History of CWD

The **history of CWD** is the following. It was **2007**, I was thinking about RPG games and there was then a problem with the words of that area of entertainment. There were a good amount of words that were lacking, at least in spanish, which is the language that I use daily. On spanish, there’s no word to differentiate a RPG system, of which I’ve invented the word, in spanish, “rolsi”, for it, related to an RPG game. An RPG system is the system that is used to play an RPG game, the rules, the ambientation of the RPG games created with that RPG system, and any other element of the RPG game. The RPG game is, instead, the specific adventure, created with an RPG system (strictly, it can be used more than one), consisting of stages, characters, objects, and a background history, that the role players play. This confusion of words was important, and CWD has been created in order to define appropriately the words that were solving it.
