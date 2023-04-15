# Awesome TNNs

This repository is an accompaniment to: *Architectures of Topological Deep Learning: A Survey on Topological Neural Networks*

*Topological Neural Networks* (TNNs) are deep learning architectures that process signals defined on topological domains. The domains of topological deep learning generalize the binary relations of graphs to *hierarchical relations* and higher-order *set-based relations*. The additional flexibility and expressivity of these architectures permits the representation of complex natural systems such as proteins, neural activity, and many-body physical systems. 

To date, the TNN literature has suffered from a lack of unification in notation and language across disparate models. This presents a real obstacle for building upon contributions in the field and applying TNNs to new problems. This repository synthesizes the literature using a single unifying notation that we use to rewrite the equations of different TNN architectures, facilitating their direct comparison.

## :brain: The Models

We rewrite model architectures using our unifying framework for most of the papers referenced in our survey. 

[Hypergraphs](/Hypergraphs.md/)

[Simplicial Complexes](/Simplicial_Complexes.md/)

[Cellular Complexes](/Celular_Complexes.md/)

[Combinatorial Complexes](/Combinatorial_Complexes.md/)

## :toolbox: The Framework

Or unifying framework consists of a four-step process, illustrated in the figure (Fig. 7 in the paper) and described in the equations below (taken from Section 2.3.1 of the paper):

<p align="center">
<img src="https://user-images.githubusercontent.com/50878631/232132437-2a5f9d3a-de37-434e-8f38-0b06e226f273.jpg" width=60% height=60%>

:red_square: **1. Message:** First, a message $m_{y \rightarrow x}^{\left(r^{\prime} \rightarrow r\right)}$ travels from a $r'$-cell $y$ to a $r$-cell $x$ through a neighborhood $k$ of $x$ denoted $\mathcal{N}\_k (x)$:

$$m_{y \rightarrow x}^{\left(r^{\prime} \rightarrow r\right)}=M_{\mathcal{N}\_k}\left(\mathbf{h}\_x^{t,(r)}, \mathbf{h}\_y^{t,(r^{\prime})}, \Theta^t \right)$$

via the function $M_{\mathcal{N}\_k}$ depicted in red in the figure. Here, $\textbf{h}\_x^{t,(r)}$ and $\textbf{h}\_y^{t,(r')}$ are features of dimension $d_r$ and $d_{r'}$ on cells $y$ and $x$ respectively, and $\Theta^t$ are learnable parameters. In the simplest case, this step looks like a neighborhood matrix $M$ propagating a feature $\mathbf{h}\_y^{t,(r')}$ on $r'$-cell $y$ to $r$-cell $x$ as: 

$$m_{y \rightarrow x}^{\left(r^{\prime} \rightarrow r\right)}= M_{xy}\cdot \textbf{h}\_y^{t,(r')} \cdot \Theta^t,$$

where $M_{xy}$ is the scalar entry of matrix $M$ at the row corresponding to cell $x$ and column corresponding to cell $y$ and $m_{y \rightarrow x}^{\left(r^{\prime} \rightarrow r\right)}$ and $\Theta$ is a $d_{r'} \times d_{r}$ matrix. If $y$ is not in the neighborhood structure of $x$, then $M_{xy}$ will be 0, and $x$ cannot receive any message from $y$. 


:orange_square: **2. Within-Neighborhood Aggregation:** Next, messages are aggregated across all cells $y$ belonging to the neighborhood $\mathcal{N}\_k(x)$:

$$ m_x^{\left(r^{\prime} \rightarrow r\right)}=A G G_{y \in \mathcal{N}_k(x)} m_{y \rightarrow x}^{\left(r^{\prime} \rightarrow r\right)}$$

resulting in the \textit{within-neighborhood aggregated message} $m_x^{\left(r^{\prime} \rightarrow r\right)}$. Here, $AGG$ is an aggregation function, depicted in orange in the figure, analogous to pooling in standard convolutional networks.

:green_square: **3. Between-Neighborhood Aggregation:** 
Then, messages are aggregated across neighborhoods in a neighborhood set $\mathcal{N}$:

$$m_x^{(r)}=A G G_{\mathcal{N}\_k \in \mathcal{N}} m_x^{\left(r^{\prime} \rightarrow r\right)}$$

where AGG is a (potentially different) aggregation function depicted in green in the figure, and $m_x^{(r)}$ is the message received by cell $x$ that triggers the update of its feature.

:blue_square: **4. Update:**
Finally, the feature on cell $x$ is updated via a function $U$ depicted in blue in the figure, which may depend on the previous feature $\textbf{h}\_x^{t,(r)}$ on cell $x$:

$$ \textbf{h}\_x^{t+1,(r)}=U\left(\textbf{h}\_x^{t,(r)}, m_x^{(r)}\right)$$

The result $\textbf{h}\_x^{t+1,(r)}$ is the updated feature on cell $x$ that is input to layer $t+1$.

## :house_with_garden: Community

We warmly welcome contributions to our open source project and invite everyone to join us in making it better. If you notice any mistakes or issues with the equations, please don't hesitate to make a pull request to help us improve the repository. Furthermore, we highly encourage authors of other TNNs not yet included to add their architectures to this growing database.
