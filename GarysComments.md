# Comments from Gary Berg-Cross on semantic resources, needs, etc

## From an email on 6/3/2016

here is a bit more on an update to relations targeted for ODM2 based on what is in [ChEBI (Chemical Entities of Biological Interest)](http://www.ontobee.org/ontology/CHEBI). There are many, m​
any entities but only a few relations:
- has functional parent
- has parent hydride
- has part
- has role
- is conjugate acid of
- is conjugate base of
- is enantiomer of
- is substituent group from
- is tautomer of

From [Chemical Information Ontology](http://www.ontobee.org/ontology/CHEMINF?iri=http://purl.obolibrary.org/obo/IAO_0000102)

Now I don't think these are all that ODM2 is interested in but it provides some idea of what other parts to Chem are using to structure their Chem knowledge.


## Here is one initial comment to follow up our telephone conversation of 2/18/2016

When we are talking about integrated queries across different domain data I think that we will need to add some relations to what is currently in ODM2 at http://vocabulary.odm2.org/relationshiptype/

These may be small enough additions to make it tractable.
Here is just one example (from the BioMed work,but similar to others):
- PARTICIPATION. The relation of participation is a species of dependence. It holds between a substance and a process: you participate in your life; in each one of your actions; in the history of your nation or regiment. A runner participates in a race. A voter participates in an election. There are different kinds of participation, which we can order along the following dimensions: 
  - active/passive (± agentive)
  - direct/mediated – complete/partial of subject (the degree to which the whole subject or only part of the subject participates) of action (the degree to which the subject is involved in the whole or only in part of the action)
  - benefactive/malefactive (± conducive to the existence of the participating subject) (This last dimension has an obvious relevance to the domain of medical ontology.) 

Related ideas to keep in mind as we model the concepts needed to integrated domain objects and processes include:
- INFLUENCE. A substance has an effect on a process
- CREATION. A process brings into being a substance: the declaration of independence creates the new state; the work of the potter creates the new vase. 
- SUSTAINING IN BEING. A process sustains in being a substance: the circulation of the blood sustains the body; 
- DEGRADATION. A process has negative effects upon a substance: eating sugar contributes to the deterioration of your teeth; the flow of water erodes the rock. 
- DESTRUCTION. A process puts a substance out of existence

There area also distinctions about part-whole relations that are probably important across domains.  
ODM2 currently has a simple hasPart relation as a container which is perhaps a carry over from object modeling and less of a GeoSci domain concept.:
hasPart	Has part	Use to indicate the resource is a container of another resource.

There is also:
isPartOf	Is part of	Use to indicate the resource is a portion of another resource.
But something can be part of something else in several ways. 
Here are a few of the ideas on part relation types that have been used in ontologies such as containment and constituent.
These help make things clearer.:

Relations that are not simple part-whole relations in the sense above

There are a number of relations easily confused with part-whole relations. Interested readers should consult [Flavours of part of]. However, a brief list includes:
- **Containment** - the fact that I am contained in my room does not mean that I am part of my room
- **Membership** -as flocks of geese and committees. Membership is not transitive. For example, the goose's leg is part of the goose but not part of the flock of geese. Slightly more awkwardly, even though we often talk of members of a committee being "part of a committee", being a member of a subcommittee that is part of a committee may, or may not, confer membership in the committee as a whole. Admittedly, whether membership is a part-whole relation is subject to debate.
- **Connections and branches** -That the lamp is connected to the main electricity system does not make it part of that system. Similarly, the tributary is not part of the river, rather a branch of the river. If we want to talk about parts, we usually speak of the "river system".
- **Constituents** - more controversially, many ontologists distinguish between the relation between clay and a statue made of clay - the clay "constitutes" or "is a constituent of" the statue, rather than being part of the statue in the same sense that the arm or leg is part of the statue. At the very least, there are a set of different issues involved in this relationship that are beyond the scope of this document.
- **subClassOf** - As discussed in Pattern 3, being a part of something is not the same as being a subclass of it.
