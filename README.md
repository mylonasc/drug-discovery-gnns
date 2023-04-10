# drug-discovery-gnns
personal project on KG learning for drug discovery

<a target="_blank" href="https://colab.research.google.com/github/mylonasc/drug-discovery-gnns/blob/main/dev/Drug_discovery_1.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>



## Open in colab [WIP]
* Compute embeddings with ProtT5 (up to 4.5k residues due to colab limmitations)
* Code for cleaning up / preproc of DrugBank (in development stage - needs cleanup)
* Sampler for drug/target neighborhoods
* Write an efficient sampler/negative sampler for graph tuples [TODO]
* Train [done - first results]
* Validate [TODO]

## First results

### Drug-protein interaction prediction
In what follows, `ProtT5` embeddings are used for the proteins and random initialization for drugs. A custom GraphSage-like sampler (with negative examples for the edges) was implemented; The depth of the neighborhood is 2. The negative samples are found by taking a simple "derangement" of the source nodes (both drugs and proteins). 

As a first example, and to show that the code works, a link prediction model was trained.

![alt text](assets/edge_class.png?raw=true)

