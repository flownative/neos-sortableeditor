# Sortable asset and references editor for Neos

sponsored by [dotpulse.ch](http://dotpulse.ch)

These two editors make assets and references sortable in the Neos inspector.
This package is just meant as a replacement for projects that need it now, a PR to Neos core is under review and
the feature should be included in the next Neos release.

To use the editors from this package, all you need to do is either replace the default editor for a type
(like `references`) in `Settings.yaml` like so:

    TYPO3:
      Neos:
        userInterface
          inspector:
            dataTypes:
              'references':
                editor: 'Flownative.NeosSortableEditor/SortableReferencesEditor'
                
Or overwrite the editor for a specific NodeType in `NodeTypes.yaml`:

    'TYPO3.Neos.NodeTypes:ContentReferences':
      properties:
        references:
          ui:
            inspector:
              editor: 'Flownative.NeosSortableEditor/SortableReferencesEditor'
