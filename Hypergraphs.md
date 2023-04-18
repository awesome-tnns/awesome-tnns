
## Schemes in the Hypergraph Domain

 
#### HyperSage (HS) <a href="#arya2020hypersage">[1]</a>

:red_square: $\quad m_{y \rightarrow z}^{(0 \rightarrow 1)} = (B_1)^T_{zy} \cdot w_y \cdot (h_y^{(0)})^p$ 

:red_square: $\quad m_z^{(0 \rightarrow 1)}  = \left(\frac{1}{\vert \mathcal{B}(z)\vert}\sum_{y \in \mathcal{B}(z)} m_{y \rightarrow z}^{(0 \rightarrow 1)}\right)^{\frac{1}{p}}$

:red_square: $\quad m_{z \rightarrow x}^{(1 \rightarrow 0)} =  (B_1)_{xz} \cdot w_z  \cdot (m_z^{(0 \rightarrow 1)})^p$

:orange_square: $\quad m_x^{(1,0)}  = \left(\frac{1}{\vert \mathcal{C}(x) \vert}\sum_{z \in \mathcal{C}(x)} m_{z \rightarrow x}^{(1 \rightarrow 0)}\right)^{\frac{1}{p}}$

:green_square: $\quad m_x^{(0)}  = m_x^{(1 \rightarrow 0)}$ 

:blue_square: $\quad h_x^{t+1, (0)} = \sigma \left(\frac{m_x^{(0)} + h_x^{t,(0)}}{\lvert m_x^{(0)} + h_x^{t,(0)}\rvert} \cdot \Theta^t\right)$ 


#### <a href="#bai2021hypergraph">[11]</a>
 
#### HyperAtten


:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(0 \rightarrow 1\rightarrow 0)}  = ((B_1 \odot att(h_z^{t,(1)}, h_y^{t,(0)})) \cdot W^{(1)} \cdot (B^T_1\odot att(h_x^{t,(0)}, h_z^{t,(1)})))_{xy} \cdot h^{t,(0)}y \cdot \Theta^t$ 

:orange_square: $\quad m{x}^{(0 \rightarrow 1 \rightarrow 0)} = \sum_{y \in \mathscr{L}\_{\uparrow}(x)} m_{y \rightarrow \{z\} \rightarrow x}^{(0 \rightarrow 1 \rightarrow 0)}$ 

:green_square: $\quad m_x^{(0)} = m_{x}^{(0 \rightarrow 1 \rightarrow 0)}$ 

:blue_square: $\quad h_x^{t+1, (0)}  = U(h_x^{t,(0)}, m_x^{(0)})$ 

#### HyperConv

:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(0 \rightarrow 1 \rightarrow 0)} = (B_1 \cdot W^{(1)} \cdot B^T_1)_{xy} \cdot h^{t,(0)}_y \cdot \Theta^t$ 

:orange_square: $\quad m_{x}^{(0 \rightarrow 1 \rightarrow 0)} = \sum_{y \in \mathcal{L}\_\uparrow(x)} m_{y \rightarrow \{z\} \rightarrow x}^{(0\rightarrow1\rightarrow0)}$ 

:green_square: $\quad m_x^{(0)} = m_x^{(0 \rightarrow 1 \rightarrow 0)}$ 

:blue_square: $\quad h_x^{t+1, (0)}  = \sigma(m_x^{(0)})$ 



#### <a href="#chien2022you">[2]</a>
 
#### AllDeepSet

:red_square: $\quad m^{(1 \rightarrow 1)}_{x \rightarrow x} = \sigma(\Theta^{t,(1 \rightarrow 1)} \cdot h_x^{t,(1)} + b^{t,(1 \rightarrow 1)})$ 

:red_square: $\quad m^{(0 \rightarrow0)}_{x \rightarrow x} = \sigma (\Theta^{t,(0 \rightarrow0)} \cdot h_x^{t,(0)} + b^{t,(0 \rightarrow0)})$ 

:red_square: $\quad m_{y\rightarrow x}^{(0 \rightarrow1)} = \sigma (\Theta^{t,(0 \rightarrow1)} \cdot h_y^{t, (0)} + b^{t,(0 \rightarrow1)})$ 

:red_square: $\quad m_{y \rightarrow x}^{(1 \rightarrow0)} = \sigma (\Theta^{t,(1 \rightarrow0)} \cdot h_y^{t, (1)} + b^{t,(1 \rightarrow0)})$ 

:orange_square: $\quad m_x^{(0 \rightarrow1)} = \sum_{y \in \mathcal{B}\_\uparrow(x)} m_{y \rightarrow x}^{(0 \rightarrow1)}$ 

:orange_square: $\quad m_x^{(1 \rightarrow0)} = \sum_{y \in \mathcal{C}\_\uparrow(x)} m_{y \rightarrow x}^{(1 \rightarrow0)}$ 

:green_square: $\quad m_x^{(1)} = W^{t,(1)}\_{\text{agg}} \cdot (m_{x \rightarrow x}^{(1 \rightarrow 1)} + m_{x}^{(0\rightarrow1)}) + b^{t,(1)}\_{\text{agg}}$ 

:green_square: $\quad m_x^{(0)} = W^{t,(0)}\_{\text{agg}} \cdot (m_{x \rightarrow x}^{(0 \rightarrow 0)} + m_{x}^{(1\rightarrow0)}) + b^{t,(0)}\_{\text{agg}}$ 

:blue_square: $\quad h_x^{t+1,(1)} = \sigma(m_x^{(1)})$ 

:blue_square: $\quad h_x^{t+1,(0)} = \sigma(m_x^{(0)})$ 

#### AllSetTransformer

Skipping message-passing due to entanglement

:orange_square: $\quad m_{\rightarrow z}^{(\rightarrow 1)} = AGG_{y \in \mathcal{B}(z)} (h_y^{t, (0)}, h_z^{t,(1)}) \quad \text{with attention}$ 

:blue_square: $\quad h_z^{t+1,(1)} = \text{LN}(m_{\rightarrow z}^{(\rightarrow 1)} + \text{MLP}(m_{\rightarrow z}^{(\rightarrow 1)} ))$ 

Edge to vertex: 

:orange_square: $\quad m_{\rightarrow x}^{(\rightarrow 0)} = AGG_{z \in \mathcal{C}(x)} (h_z^{t+1,(1)}, h_x^{t,(0)}) \quad \text{with attention}$ 

:blue_square: $\quad h_x^{t+1,(0)} = \text{LN}(m_{\rightarrow x}^{(\rightarrow 0)} + \text{MLP}(m_{\rightarrow x}^{(\rightarrow 0)} ))$



#### HyperGat, <a href="#ding2020less">[8]</a>

:red_square: $\quad m_{y \rightarrow z}^{(0 \rightarrow 1) } = (B^T_1\odot att(h_{y \in \mathcal{B}(z)}^{t,(0)}))\_{zy} \cdot h^{t,(0)}y \cdot \Theta^{t,(0)}$ 

:orange_square: $\quad m_z^{(1)} = \sigma(\sum_{y \in \mathcal{B}(z)} m_{y \rightarrow z}^{(0 \rightarrow 1)})$ 

:red_square: $\quad m_{z \rightarrow x}^{(1 \rightarrow 0)}  = (B_1 \odot att(h_{z \in \mathcal{C}(x)}^{t,(1)}))\_{xz} \cdot m_{z}^{(1)} \cdot \Theta^{t,(1)}$ 

:orange_square: $\quad m_{x}^{(0)}  = \sum_{z \in \mathcal{C}(x)} m_{z \rightarrow x}^{(1\rightarrow0)}$ 

:green_square: $\quad m_x = m_{x}^{(0)}$ 

:blue_square: $\quad h_x^{t+1, (0)} = \sigma(m_x)$


#### Hypergraph Networks with Hyperedge Neurons (HNHN), <a href="#dong2020hnhn">[12]</a>

:red_square: $\quad m_{y \rightarrow x}^{(0 \rightarrow 1)} = \sigma((B_1^T \cdot W^{(0)})\_{xy} \cdot h_y^{t,(0)} \cdot \Theta^{t,(0)} + b^{t,(0)})$ 

:red_square: $\quad m_{y \rightarrow x}^{(1 \rightarrow 0)}  = \sigma((B_1 \cdot W^{(1)})\_{xy} \cdot h_y^{t,(1)} \cdot \Theta^{t,(1)} + b^{t,(0)})$ 

:orange_square: $\quad m_x^{(0 \rightarrow 1)}  = \sum_{y \in \mathcal{B}(x)} m_{y \rightarrow x}^{(0 \rightarrow 1)}$ 

:orange_square: $\quad m_x^{(1 \rightarrow 0)}  = \sum_{y \in \mathcal{C}(x)} m_{y \rightarrow x}^{(1 \rightarrow 0)}$ 

:green_square: $\quad m_x^{(0)}  = m_x^{(1 \rightarrow 0)}$ 

:green_square: $\quad m_x^{(1)}  = m_x^{(0 \rightarrow 1)}$ 

:blue_square: $\quad h_x^{t+1,(0)}  = \sigma(m_x^{(0)})$ 

:blue_square: $\quad h_x^{t+1,(1)} = \sigma(m_x^{(1)})$


#### Hypergraph Message Passing Neural Networks (HMPNN), <a href="#heydari2022message">[10]</a>

:red_square: $\quad m_{{y \rightarrow z}}^{(0 \rightarrow 1)} = M_\mathcal{C} (h_y^{t,(0)}, h_z^{t, (1)})$ 

:orange_square: $\quad m_{z'}^{(0 \rightarrow 1)} = AGG'{y \in \mathcal{B}(z)} m_{y \rightarrow z}^{(0\rightarrow1)}$ 

:orange_square: $\quad m_{z}^{(0 \rightarrow 1)} = AGG_{y \in \mathcal{B}(z)} m_{y \rightarrow z}^{(0 \rightarrow 1)}$ 

:red_square: $\quad m_{z \rightarrow x}^{(1 \rightarrow0)} = M_\mathcal{B}(h_z^{t,(1)}, m_z^{(1)})$ 

:orange_square: $\quad m_x^{(1 \rightarrow0)} = AGG_{z \in \mathcal{C}(x)} m_{z \rightarrow x}^{(1 \rightarrow0)}$ 

:green_square: $\quad m_x^{(0)} = m_x^{(1 \rightarrow 0)}$ 

:green_square: $\quad m_z^{(1)}  = m_{z'}^{(0 \rightarrow 1)}$ 

:blue_square: $\quad h_x^{t+1, (0)} = U^{(0)}(h_x^{t,(0)}, m_x^{(0)})$ 

:blue_square: $\quad h_z^{t+1,(1)} = U^{(1)}(h_z^{t,(1)}, m_{z}^{(1)})$


#### UniGNN, <a href="#huang2021unignn">[6]</a>
 
#### UniGAT

:red_square: $\quad m_{y \rightarrow z}^{(0 \rightarrow 1)} = (B^T_1)\_{zy} \cdot h^{t,(0)}_y$ 

:orange_square: $\quad m_z^{(0\rightarrow1)} = \sum_{y \in \mathcal{B}(z)} m_{y \rightarrow z}^{(0 \rightarrow 1)}$ 

:red_square: $\quad m_{z \rightarrow x}^{(1 \rightarrow 0)} = ((B_1 \odot att(h_{z \in \mathcal{C}(x)}^{t,(1)})))\_{xz} \cdot m_{z}^{(0\rightarrow1)} \cdot \Theta^{t,(1)}$ 

:orange_square: $\quad m_{x}^{(1 \rightarrow0)}  = \sum_{z \in \mathcal{C}(x)} m_{z \rightarrow x}^{(1\rightarrow0)}$ 

:green_square: $\quad m_x^{(0)}  = m_{x}^{(1 \rightarrow 0)}$ 

:blue_square: $\quad h_x^{t+1, (0)} = m_x^{(0)}$


#### UniGCN

:red_square: $\quad m_{y \rightarrow z}^{(0 \rightarrow 1)}  = B_1^T \cdot h_y^{t, (0)}$ 

:orange_square: $\quad m_z^{(0 \rightarrow 1)}  = \sum_{y \in \mathcal{B}(z)} m_{y \rightarrow z}^{(0 \rightarrow 1)}$ 

:red_square: $\quad m_{z \rightarrow x}^{(1 \rightarrow 0)} = B_1^{t,(1)} \cdot w^{(1)} \cdot  m_z^{(0 \rightarrow 1)} \cdot \Theta^t$ 

:orange_square: $\quad m_x^{(1 \rightarrow 0)}  = \sum_{y \in \mathcal{C}(x)} m_{z \rightarrow x}^{(1 \rightarrow 0)}$ 

:green_square: $\quad m_x^{(0)}  = m_x^{(1\rightarrow0)}$ 

:blue_square: $\quad h_x^{t+1,(0)}  = m_x^{(0)}$


#### UniGiN

:red_square: $\quad m_{y \rightarrow z}^{(0 \rightarrow 1)}  = B_1^T \cdot h_y^{t, (0)}$ 

:orange_square: $\quad m_z^{(0 \rightarrow 1)}  = \sum_{y \in \mathcal{B}(z)} m_{y \rightarrow z}^{(0 \rightarrow 1)}$ 

:red_square: $\quad m_{z \rightarrow x}^{(1 \rightarrow 0)}  = B_1 \cdot m_z^{(0 \rightarrow 1)}$ 

:orange_square: $\quad m_{x}^{(1\rightarrow0)}  = \sum_{z \in \mathcal{C}(x)} m_{z \rightarrow x}^{(1\rightarrow0)}$ 

:green_square: $\quad m_x^{(0)}  = m_{x}^{(1\rightarrow0)}$ 

:blue_square: $\quad h_x^{t+1,(0)}  = \Theta^t \cdot ((1+\theta)\cdot h_x^{t,(0)}+m_x^{(0)})$


#### UniSAGE

:red_square: $\quad m_{y \rightarrow z}^{(0 \rightarrow 1)}  = (B_1^T)\_{zy} \cdot h_y^{t, (0)}$ 

:orange_square: $\quad m_z^{(0 \rightarrow 1)}  = \sum_{y \in \mathcal{B}(z)} m_{y \rightarrow z}^{(0 \rightarrow 1)}$ 

:red_square: $\quad m_{z \rightarrow x}^{(1 \rightarrow 0)}  = B_1 \cdot m_z^{(0 \rightarrow 1)}$ 

:orange_square: $\quad m_{x}^{(1\rightarrow0)}  = AGG_{z \in \mathcal{C}(x)} m_{z \rightarrow x}^{(1\rightarrow0)}$ 

:green_square: $\quad m_x^{(0)}  = m_{x}^{(1\rightarrow0)}$ 

:blue_square: $\quad h_x^{t+1,(0)} = \Theta^t \cdot (h_x^{t,(0)}+m_x^{(0)})$

#### UniGCNII

:red_square: $\quad m_{y \rightarrow z}^{(0 \rightarrow 1)} = (B_1^T)\_{zy} \cdot h_y^{t, (0)}$ 

:orange_square: $\quad m_z^{(0 \rightarrow 1)}  = \sum_{y \in \mathcal{B}(z)} m_{y \rightarrow z}^{(0 \rightarrow 1)}$ 

:red_square: $\quad m_{z \rightarrow x}^{(1 \rightarrow 0)}  = B_1 \cdot m_z^{(0 \rightarrow 1)}$ 

:orange_square: $\quad m_{x}^{(1\rightarrow0)}  = \frac{1}{\sqrt{d_x}}\sum_{z \in \mathcal{C}(x)} \frac{1}{\sqrt{d_z}}m_{z \rightarrow x}^{(1\rightarrow0)}$ 

:green_square: $\quad m_x^{(0)}  = m_x^{(1 \rightarrow 0)}$ 

:blue_square: $\quad m_x^{(0)}  = ((1-\theta_1)I + \theta_1 W)((1-\theta_2)m_x^{(0)} + \theta_2 \cdot h_x^{t,(0)})$



#### Dynamic Hypergraph Neural Networks (DHNN), <a href="#jiang2019dynamic">[5]</a>

:orange_square: $\quad m_{\rightarrow z}^{\rightarrow 1} = \text{AGG}\_{y \in \mathcal{B}(z)}(h_y^{0, t})$ 

:blue_square: $\quad h_z^{1, t+1} = \sigma(m_{\rightarrow z}^{\rightarrow 1})$ 

:red_square: $\quad m_{z \rightarrow x}^{1 \rightarrow 0} = M_\mathcal{B}(att(h_z^{1, t+1}), h_z^{1, t+1})$ 

:orange_square: $\quad m_{\rightarrow x}^{\rightarrow 0} = \sum_{z \in \mathcal{C}(x)} m_{z \rightarrow x}^{0\rightarrow 1}$ 

:blue_square: $\quad {h_x^{0, t+1}} = \text{MLP}(m_{\rightarrow x}^{\rightarrow 0})$


#### Equivariant Hypergraph Neural Networks (EHNN), <a href="#kim2022equivariant">[7]</a>

Let $B_{k \rightarrow L}^I$ represent the order-I boundary matrix from cells of rank $k$ to cells of rank $L$. We say that a hyperedge of size L is an order-I boundary of a hyperedge of size k if the hyperedges intersect on exactly I elements.
 
#### EHNN-MLP

For the neighborhood structure I, which is an order-I boundary: 

:red_square: $\quad m_{y \rightarrow x}^{k \rightarrow l, B_k^I} = \text{MLP}\_{\Theta_1}(h_y^{t,(k)})$ 

Aggregation within each intra-neighborhood structure $B_k^I$: 

:orange_square: $\quad m_{\rightarrow x}^{k \rightarrow l, B_k^I} = \sum_{y \in B_k^I(x)} m_{y \rightarrow x}^{k \rightarrow l, B_k^I}$ 

Aggregation inter-neighborhood structures $B_k^I$'s with same intersection $I$ but different ranks: 

:green_square: $\quad m_{\rightarrow x}^{\rightarrow l, \{B_k^I\}\_k} = \sum\_{k \leq K} m_{y \rightarrow x}^{k \rightarrow l, B_k^I}$ 

Aggregation inter-neighborhood structure} B_k^{I}\text{’s with different intersections $I$ 

:green_square: $\quad m_{\rightarrow x}^{\rightarrow l, \{B_k^I\}} = \sum_{I \geq 0} \text{MLP}\_{\Theta_2} (m_{\rightarrow x}^{\rightarrow l, \{B_k^I\}\_k})$ 

:blue_square: $\quad m_{\rightarrow x}^{\rightarrow l} = \text{MLP}\_{\Theta_3}(m_{\rightarrow x}^{\rightarrow l, \{B_k^I\}}) + b(l)$

#### EHNN-Transformer    

For the neighborhood structure I, which is an order-I boundary: 

:red_square: $\quad m_{y \rightarrow x}^{k \rightarrow l, B_k^I} = \text{MLP}\_{\Theta_1}(h_y^{t,(k)})$ 

We add attention: 

:red_square: $\quad m_{y \rightarrow x}^{k \rightarrow l, B_k^I, h} = \alpha_h(m_{y \rightarrow x}^{k \rightarrow l, B_k^I}) \cdot m_{y \rightarrow x}^{k \rightarrow l, B_k^I}$

Aggregation within each intra-neighborhood structure $B_k^I$: 

:orange_square: $\quad m_{\rightarrow x}^{k \rightarrow l, B_k^I, h}  = \sum_{y \in B_k^I(x)} m_{y \rightarrow x}^{k \rightarrow l, B_k^I, h}$ 

Aggregation inter-neighborhood structures $B_k^I$'s with same intersection $I$ but different ranks: 

:green_square: $\quad m_{\rightarrow x}^{\rightarrow l, \{B_k^I\}\_k, h} = \sum_{k \leq K} m_{y \rightarrow x}^{k \rightarrow l, B_k^I, h}$ 

Aggregation inter types of attentions, i.e. across $h$’s (”number of heads”): 

:green_square: $\quad m_{\rightarrow x}^{\rightarrow l, \{B_k^I\}\_k} = \sum_{h} m_{\rightarrow x}^{\rightarrow l, \{B_k^I\}\_k, h} \cdot \Theta_h$ 

Aggregation inter-neighborhood structure $B_k^{I}$’s with different intersections $I$

:green_square: $\quad m_{\rightarrow x}^{\rightarrow l, \{B_k^I\}}  = \sum_{I \geq 0} \text{MLP}\_{\Theta_2} (m_{\rightarrow x}^{\rightarrow l, \{B_k^I\}\_k})$ 

:blue_square: $\quad m_{\rightarrow x}^{\rightarrow l}  = \text{MLP}\_{\Theta_3}(m_{\rightarrow x}^{\rightarrow l, \{B_k^I\}}) + b(l)$ 

:blue_square: $\quad m_{\rightarrow x} = \text{ATTN}(m_{\rightarrow x}) + \text{MLP}\_{\Theta_4}(\text{ATTN}(m_{\rightarrow x}))$



#### Heterogenous Hypergraph Neural Network (HHNN), <a href="#li2022heterogeneous">[13]</a>


:red_square: $\quad m_{y \rightarrow z}^{(0 \rightarrow 1) } = (B^T_1\odot att(h_{y \in \mathcal{B}(z), }^{t,(0)}, h_z^{t,(1)}))\_{zy} \cdot h^{t,(0)}\_y$ 

:orange_square: $\quad m_z^{(1)} = \sigma(\sum_{y \in \mathcal{B}(z)} m_{y \rightarrow z}^{(0 \rightarrow 1)})$ 

:red_square: $\quad m_{z \rightarrow x}^{(1 \rightarrow 0)} = (B_1 \odot att(h_{z \in \mathcal{C}(x)}^{t,(1)}, h_x^{t,(0)}))\_{xz} \cdot m_{z}^{(1)}$ 

:orange_square: $\quad m_{x}^{(0)} = \sum_{z \in \mathcal{C}(x)} m_{z \rightarrow x}^{(1\rightarrow0)}$ 

:green_square: $\quad m_x = m_{x}^{(0)}$ 

:blue_square: $\quad h_x^{t+1, (0)}  = \sigma(m_x)$


#### Hypergraph Transformer Neural Networks (HGTN), <a href="#li2022hypergraph">[9]</a>

:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(0 \rightarrow 1 \rightarrow 0)} = (B_1 \cdot W^{(1)} \cdot B^T_1)\_{xy} \cdot h^{t,(0)}\_y \cdot \Theta^t$ 

:orange_square: $\quad m_{x}^{(0 \rightarrow 1 \rightarrow 0)} = \sum_{y \in \mathcal{L}\_\uparrow(x)} m_{y \rightarrow \{z\} \rightarrow x}^{(0\rightarrow1\rightarrow0)}$ 

:green_square: $\quad m_x^{(0)} = m_x^{(0 \rightarrow 1 \rightarrow 0)}$ 

:blue_square: $\quad h_x^{t+1, (0)} = \sigma(m_x^{(0)})$


#### Session-based Hypergraph Attention Network for Recommendation (SHARE), <a href="#wang2021session">[4]</a>

:red_square: $\quad m_{y \rightarrow z}^{(0 \rightarrow 1)} = (B^T_1\odot att(h_{y \in \mathcal{B}(z)}^{t,(1)}))\_{zy} \cdot h^{t,(0)}\_y \cdot \Theta^{t,(0 \rightarrow 1)}$ 

:orange_square: $\quad m_z^{(0\rightarrow1)} = \sum_{y \in \mathcal{B}(z)} m_{y \rightarrow z}^{(0 \rightarrow 1)}$ 

:red_square: $\quad m_{z \rightarrow x}^{(1 \rightarrow 0)} = (B_1 \odot att(h_{z \in \mathcal{C}(x)}^{t,(1)}))\_{xz} \cdot m_{z}^{(0\rightarrow1)} \cdot \Theta^{t,(1 \rightarrow 0)}$ 

:orange_square: $\quad m_{x}^{(1 \rightarrow0)}  = \sum_{z \in \mathcal{C}(x)} m_{z \rightarrow x}^{(1\rightarrow0)}$ 

:green_square: $\quad m_x^{(0)} = m_{x}^{(1 \rightarrow 0)}$ 

:blue_square: $\quad h_x^{t+1, (0)} = m_x^{(0)}$


#### Hypergraph Convolutional Recurrent Neural Network, <a href="#yi2020hypergraph">[3]</a>
 
#### HGC-RNN-M

:red_square: $\quad m_{y \rightarrow z}^{(0 \rightarrow 1)} = B_1^T \cdot h_y^{t,(0)} \cdot \Theta^{(0)}$ 

:orange_square: $\quad m_{z}^{(0\rightarrow1)} = \frac{1}{\vert\mathcal{B}(z)\vert} \sum_{y \in \mathcal{B}(z)} m_{y \rightarrow z}^{(0\rightarrow1)}$ 

:red_square: $\quad m_{z \rightarrow x}^{(1\rightarrow0)} = B_1 \cdot m_z^{(0\rightarrow1)} \cdot \Theta^{(1)}$ 

:orange_square: $\quad m_x^{(1\rightarrow0)} = \frac{1}{\vert \mathcal{C}(x) \vert} \sum_{z \in \mathcal{C}(x)} m_{z \rightarrow x}^{(1\rightarrow0)}$ 

:green_square: $\quad m_x^{(0)} = m_x^{(1\rightarrow0)}$ 

:blue_square: $\quad h_x^{t+1, (0)} = \Theta^{\text{update}} \cdot (h_x^{t,(0)}\vert \vert m_x^{(0)})+b^{\text{update}}$

#### HGC-RNN-A

:red_square: $\quad m_{y \rightarrow z}^{(0\rightarrow1)} = B_1^T \cdot h_y^{t,(0)} \cdot \Theta^{(0 \rightarrow 1)}$ 

:orange_square: $\quad m_{z}^{(0\rightarrow1)} = \frac{1}{\vert \mathcal{B}(z) \vert} \sum_{y \in \mathcal{B}(z)} m_{y \rightarrow z}^{(0\rightarrow1)}$ 

:red_square: $\quad m_{z \rightarrow x}^{(1 \rightarrow 0)} = B_1\odot att(m_{z \in \mathcal{C}(x)}^{(0\rightarrow1)}, h_x^{t,(0)}) \cdot m_z^{(0\rightarrow1)} \cdot \Theta^{(1 \rightarrow 0)}$ 

:orange_square: $\quad m_x^{(1\rightarrow0)} = \frac{1}{\vert \mathcal{C}(x) \vert} \sum_{z \in \mathcal{C}(x)} m_{z \rightarrow x}^{(1\rightarrow0)}$ 

:green_square: $\quad m_x^{(0)} = m_x^{(1\rightarrow0)}$ 

:blue_square: $\quad h_x^{t+1, (0)} = \Theta^{\text{update}} \cdot (h_x^{t,(0)}\vert \vert m_x^{(0)})+b^{\text{update}}$

# Graphical illustrations

We can make graphical illustrations, called tensor diagrams, from the equations above, as outlined in Section 2.3.2 of the paper.
![Screen Shot 2023-04-14 at 6 01 31 PM](https://user-images.githubusercontent.com/8267869/232175387-1e32b6f7-df76-4e12-8f38-4123f7d2a846.png)

We use them to describe each TNN (Fig. 10 of the paper), allowing even the most complex architectures on hypergraphs to be compared with other models from different domains.

## References
1. <a id="arya2020hypersage"></a>Devanshu Arya, Deepak K Gupta, Stevan Rudinac and Marcel Worring. HyperSAGE: Generalizing inductive representation learning on hypergraphs. arXiv preprint arXiv:2010.04558. 2020
2. <a id="chien2022you"></a>Eli Chien, Chao Pan, Jianhao Peng and Olgica Milenkovic. You are AllSet: A Multiset Function Framework for Hypergraph Neural Networks. International Conference on Learning Representations. 2022
3. <a id="yi2020hypergraph"></a>Jaehyuk Yi and Jinkyoo Park. Hypergraph convolutional recurrent neural network. Proceedings of the 26th ACM SIGKDD International Conference on Knowledge Discovery & Data Mining. 2020
4. <a id="wang2021session"></a>Jianling Wang, Kaize Ding, Ziwei Zhu and James Caverlee. Session-based Recommendation with Hypergraph Attention Networks. Proceedings of the 2021 SIAM International Conference on Data Mining (SDM). 2021
5. <a id="jiang2019dynamic"></a>Jianwen Jiang, Yuxuan Wei, Yifan Feng, Jingxuan Cao and Yue Gao. Dynamic Hypergraph Neural Networks. Proceedings of International Joint Conferences on Artificial Intelligence. 2019
6. <a id="huang2021unignn"></a>Jing Huang and Jie Yang. UniGNN: a Unified Framework for Graph and Hypergraph Neural Networks. Proceedings of the Thirtieth International Joint Conference on Artificial Intelligence, {IJCAI-21}. 2021
7. <a id="kim2022equivariant"></a>Jinwoo Kim, Saeyoon Oh, Sungjun Cho and Seunghoon Hong. Equivariant Hypergraph Neural Networks. Computer Vision-ECCV 2022: 17th European Conference, Tel Aviv, Israel, October 23-27, 2022, Proceedings, Part XXI. 2022
8. <a id="ding2020less"></a>Kaize Ding, Jianling Wang, Jundong Li, Dingcheng Li and Huan Liu. Be More with Less: Hypergraph Attention Networks for Inductive Text Classification. Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP). 2020
9. <a id="li2022hypergraph"></a>Mengran Li, Yong Zhang, Xiaoyong Li, Yuchen Zhang and Baocai Yin. Hypergraph Transformer Neural Networks. ACM Transactions on Knowledge Discovery from Data (TKDD). 2022
10. <a id="heydari2022message"></a>Sajjad Heydari and Lorenzo Livi. Message Passing Neural Networks for Hypergraphs. Proceedings of 31st International Conference on Artificial Neural Networks, Part II. 2022
11. <a id="bai2021hypergraph"></a>Song Bai, Feihu Zhang and Philip HS Torr. Hypergraph convolution and hypergraph attention. Pattern Recognition. 2021
12. <a id="dong2020hnhn"></a>Yihe Dong, Will Sawin and Yoshua Bengio. HNHN: Hypergraph Networks with Hyperedge Neurons. ICML Graph Representation Learning and Beyond Workshop. 2020
13. <a id="li2022heterogeneous"></a>Yongkang Li, Zipei Fan, Jixiao Zhang, Dengheng Shi, Tianqi Xu, Du Yin, Jinliang Deng and Xuan Song. Heterogeneous Hypergraph Neural Network for Friend Recommendation with Human Mobility. Proceedings of the 31st ACM International Conference on Information & Knowledge Management. 2022
