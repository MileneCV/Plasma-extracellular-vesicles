# Plasma Extracellular vesicles _ pathway plot
Repository that will be linked with RStudio

## Exel file 
View (X15_cluster_pathway_category)

![image](https://user-images.githubusercontent.com/112773242/226803745-167c6bc9-2925-4c50-993c-668b6df47568.png)


## Code R 
X15_cluster_pathway_category%>% ggplot(aes(x = fct_inorder( Comparison), y = fct_inorder(Term), color = pvalue)) + geom_point(aes(size = Fold_Enrichment)) +   scale_color_gradient(low="blue", high="red", guide = guide_colorbar(title = "p-value")) +   guides(size = guide_legend(title = "Fold Enrichment")) + labs(x = "Clusters") + labs(y = " Pathways") + facet_wrap(~category, scales = "free", ncol = 1, strip.position = "top")

## Plot 

![image](https://user-images.githubusercontent.com/112773242/226802646-13a673c8-9f70-4837-aca2-f21638e2a66e.png)
