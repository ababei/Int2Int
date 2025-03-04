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
--pca_legend
```
as either 0 (default) or 1. Choose 1 to add a legend to your plot that specifies each separate color.

```
--pca_labels
```
Determines the coloring of labels in the PCA plot. 
By default, labels are colored using a rainbow gradient:
- Based on tokens if `pca_initial == 1`
- Based on input indices when plotting hidden states (`pca_initial == 0`)
- To use custom label coloring and manually group labels into clusters with the same color, provide a path to a JSON file containing a dictionary:
  - Keys: Integers in the range `[0, n-1]`, where `n` is the number of colors.
  - Values: Lists of either:
    - Words (if `pca_initial == 1`) to assign the same color to related words.
    - Input indices (if `pca_initial == 0`) to assign the same color to specific input positions.