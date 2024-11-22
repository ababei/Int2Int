Adding additional functionality for plotting 2D PCA on learned embeddings and representations in Int2Int https://github.com/f-charton/Int2Int

## Parameters to add to parser

```
--pca_id 
```
as the name of the experiment to be added to the plot

```
--pca_plot
```
as either 0 (default) or 1. Choose 1 for plotting some 2D PCA with arguments to follow

```
--pca_initial
```
as either 0 (default) or 1. Choose 1 for plotting the initial embedding, otherwise 0 for plotting hidden state representations.

```
--pca_layer
```
If pca_initial is 0, then pick which layer. From 1 to 3 for intermediate layers, -1 to default to the last layer.

```
--pca_bychar
```
If pca_initial is 0, this will bunch the dots on the plot by a given characteristic. The default is 0, for bunching by sequences. 1 is for averaging by word. 

```
--pca__labels
```
Give the string presentation of a dictionary. Keys will be labels to color the pca plot by, values are lists of the indices of the dots for a given color.

