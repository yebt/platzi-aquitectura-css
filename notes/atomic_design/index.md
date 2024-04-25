<!--
vim:spell wrap ts=2 sw=2
-->
# Atomic Design

  - Atom
    Single
    Simple structure, indivisible
    Like: input, label, button
  - molecule
    Multiple atoms
    Collection of atoms to build a simple component, relatively simple
    like: form section (build with label, input, button )
  - Organism
    Multiple Molecules
    Complex structure, mix atoms and molecules
    like: header,(navbar (molecule), link(atom), logo(atom) )
  - Template
    Layout structure
    Put a components inside a design to show the structure, manage the general struct
    Donde va ir los organismos
  - Page
    Pass information to template

## Folder Structure


```
src/
  components/
    atms/
      Descriptions
      ErrorMessage
      Loading
      Title
      AtomImageButton
      AtomNextShuffle
      AtomSumSub
      AtomTrainingButton
    Molecules/
      Amentiles
      Carousel
      PlaceCard
      Rating
      Review
      MoleculeLevel
      MoleculeOption
    Organism/
      Footer
      Header
      Map
      PlaceDetails
      OrganismModal
    Pages/ --> View/
      layout
    Templates/ --> View/
      PlaceList
      Ratings
      ReviewContainer

```
