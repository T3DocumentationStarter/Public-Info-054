.. Tip - just do it:
      don't use TABs (= \t, tabulators)
      replace each TAB by *three blanks* (enable RegExp for Search and Replace in your IDE)
      set TAB width and indentation to THREE in your IDE
      set 'Use blanks instead of TABs' in your IDE


.. With the following include we import some definition. We do this in each and every file.
   so we can change the definition at a single place. Use the relative path to the Includes.txt file,
   which may look as well like ../../../Includes.txt for a deeply nested source file.

.. include:: Includes.txt


.. Usually we define 'php' as default highlight language in Includes.txt.
   With the following 'highlight' directive we switch to reStructuredText as default highlight language.

.. highlight:: rst


.. The following, first section (= headline) is the 'Document Title'.


================
Sven Wiener Docs
================


.. The following is 'field list' which is rendered as a horizontal table.
   Think of it as key-value pairs.


:Writing here:    Sven Wiener
:Rendered:        |today|
:Buildinfo:       `buildinfo <_buildinfo>`_

__ https://docs.typo3.org/typo3cms/drafts/github/T3DocumentationStarter/Public-Info-001/TeachingDocs/StarterManuals/

.. _Martin: martin.bless@mbless.de

.. attention::

   This is my private documentation-library, where I collect my sodesnippets and knowledge. Good parts which I wanna share, I will give to Martin and der Documentation-Team, to put that into the main-documentation.

---------------------------------------------


.. _Infos von Martin:

Wir führen auch eine Liste `"Wer ist wo?" hier
<https://docs.typo3.org/typo3cms/drafts/github/T3DocumentationStarter/Public-Info-001/TeachingDocs/StarterManuals/Index.html#who-is-where>`__.
      
Wenn mir mehr einfällt oder Fragen auftauchen schreibe ich mehr in der
`Mastervorlage des Starter-Projektes`__. Dort kann man also bei Bedarf
reinschauen.

Für Anregungen, was man mit diesem Starter Projekt machen kann, schau
dir meins an. Das Arbeiten damit ist so einfach und einladend,
dass ich es selbst ständig benutze. **Tipp:** `Guck dir zur Anregung mal
Martin's Starterprojekt an!
<https://github.com/T3DocumentationStarter/Public-Info-001>`__

Und, **Tipp!**, beobachte `die wachsende Liste der Dokumentations-Helden!
<https://docs.typo3.org/typo3cms/drafts/github/T3DocumentationStarter/Public-Info-001/TeachingDocs/StarterManuals/Index.html>`__

.. _Sphinx: http://www.sphinx-doc.org/

.. Dies sind anonyme Hyperlinks. Jeder Link im Text, der durch zwei anhängende Unterstriche
   gebildet wird, verbraucht den nächsten aus dieser Liste.

__ https://docs.typo3.org/typo3cms/RenderTYPO3DocumentationGuide/ProjectsOnGithub/Index.html
__ https://docs.typo3.org/typo3cms/drafts/github/T3DocumentationStarter/Public-Info-000/reStructuredText/Index.html
__ https://docs.typo3.org/typo3cms/drafts/github/T3DocumentationStarter/Public-Info-000/

.. toctree::
   :hidden:

   Sitemap/Index
   SystemExtensions/Index
   Extbase/Index
   Knowledgebase/Index
   Linktargets/Index


