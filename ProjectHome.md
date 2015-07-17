A domain-specific language (DSL) analysis tool that provides three analysis techniques for your (currently Xtext-based) DSL:

  * _Instance analysis_ – summarizes the frequency of use of metamodel elements.

  * _Relationship analysis_ – generates clusters based on the co-occurrence of metamodel elements in the observed models.

  * _Clone analysis_ – reports the extent of cloning within the models.

The tool evaluates the in-memory representation of Xtext DSL instances, which is stored as EMF models. Because the tool evaluates the EMF model representation, non-Xtext-based EMF models can also use the first two analysis techniques (i.e., instance and relationship).

#### Disclaimer ####

  * The instance analysis results layout is inspired by the [EMF-Statistics-View](https://github.com/mark-christiaens/EMF-Statistics-View).
  * The clustering process utilizes [Weka](http://www.cs.waikato.ac.nz/ml/weka/), which is licensed under the GNU General Public License.