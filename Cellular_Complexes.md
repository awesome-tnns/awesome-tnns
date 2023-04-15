# Schemes in the Cellular Complex Domain

 
#### CW Network (CWN), <a href="#bodnar2021weisfeiler">[1]</a>


:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(r \rightarrow r' \rightarrow r)} = M_{\mathcal{L}\uparrow}(h_x^{t,(r)}, h_y^{t,(r)}, h_z^{t,(r')})$ 

:red_square: $\quad m_{y \rightarrow x}^{(r'' \rightarrow r)} = M_{\mathcal{B}}(h_x^{t,(r)}, h_y^{t,(r'')})$ 

:orange_square: $\quad m_x^{(r'' \rightarrow r)} = AGG_{y \in \mathcal{B}(x)} m_{y \rightarrow x}^{(r'' \rightarrow r)}$ 

:orange_square: $\quad m_x^{(r \rightarrow r' \rightarrow r)} = AGG_{y \in \mathcal{L}(x)} m_{y \rightarrow \{z\} \rightarrow x}^{(r \rightarrow r' \rightarrow r)}$ 

:green_square: $\quad m_x^{(r)} = AGG_{\mathcal{N}\_k \in \mathcal{N}} (m_x^k)$ 

:blue_square: $\quad h_x^{t+1,(r)} = U\left(h_x^{t,(r)}, m_x^{(r)}\right)$


#### Cell Attention Network (CAN), <a href="#giusti2022cell">[2]</a>


:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(1 \rightarrow 2 \rightarrow 1)} = \sigma\left((L_{\uparrow,1} \odot att(h_{y \in \mathcal{L}\uparrow(x)}^{t,(1)}, h_x^{t,(1)}))\_{xy} \cdot h_y^{t,(1)} \cdot \Theta^{t,(1 \rightarrow 2 \rightarrow 1)} \right)$ 

:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(1 \rightarrow 0 \rightarrow 1)} = \sigma \left((L_{\downarrow,1} \odot att(h_{y \in \mathcal{L}\downarrow(x)}^{t,(1)}, h_x^{t,(1)}))\_{xy} \cdot h_y^{t,(1)} \cdot \Theta^{t,(1 \rightarrow 0 \rightarrow 1)} \right)$ 

:red_square: $\quad m^{(1 \rightarrow 1)}\_{x \rightarrow x} = \sigma\left((1+\epsilon)\cdot h_x^{t, (1)} \cdot \Theta^{t,(1 \rightarrow 1)} \right)$ 

:orange_square: $\quad m_{x}^{(1 \rightarrow 2 \rightarrow 1)} = \sum_{y \in \mathcal{L}\_\uparrow(x)}m_{y \rightarrow \{z\} \rightarrow x}^{(1 \rightarrow 2 \rightarrow 1)}$ 

:orange_square: $\quad m_{x}^{(1 \rightarrow 0 \rightarrow 1)} = \sum_{y \in \mathcal{L}\_\downarrow(x)}m_{y \rightarrow \{z\} \rightarrow x}^{(1 \rightarrow 0 \rightarrow 1)}$ 

:orange_square: $\quad m^{(1 \rightarrow 1)}\_{x} = m^{(1 \rightarrow 1)}\_{x \rightarrow x}$ 

:green_square: $\quad m_x^{(1)} = m_x^{(1 \rightarrow 1)} + m_{x}^{(1 \rightarrow 2 \rightarrow 1)} + m_{x}^{(1 \rightarrow 0 \rightarrow 1)}$ 

:blue_square: $\quad h_x^{t+1, (1)} = \sigma(\theta_{att} \cdot m_x^{(1)})\cdot m_x^{(1)}$


#### Convolutional Cell Complex Networks (CCXN), <a href="#hajij2020cell">[3]</a>
 
 
#### Adjacency Message-Passing Scheme 
:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(0 \rightarrow 1 \rightarrow 0)} = M_{\mathcal{L}\_\uparrow}^t(h_x^{t,(0)}, h_y^{t,(0)}, \Theta^{t,(y \rightarrow x)})$ 

:orange_square: $\quad m_x^{(0 \rightarrow 1 \rightarrow 0)} = AGG_{y \in \mathcal{L}\_\uparrow(x)}(m_{y \rightarrow \{z\} \rightarrow x}^{0 \rightarrow 1 \rightarrow 0})$ 

:green_square: $\quad m_x^{(0)} = m_x^{(0 \rightarrow 1 \rightarrow 0)}$ 

:blue_square: $\quad h_x^{t+1,(0)} = U^{t}(h_x^{t,(0)}, m_x^{(0)})$


#### Co-Adjacency Message Passing Scheme 

:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(r \rightarrow r'' \rightarrow r)} = M_{\mathcal{L}\_\downarrow}^t(h_x^{t,(r)}, h_y^{t,(r)}, \Theta^{t,(y \rightarrow x)})$ 

:orange_square: $\quad m_x^{(r \rightarrow r'' \rightarrow r)} = AGG_{y \in \mathcal{L}\_\downarrow(x)}(m_{y \rightarrow \{z\} \rightarrow x}^{r \rightarrow r'' \rightarrow r})$ 

:green_square: $\quad m_x^{(0)} = m_x^{(r \rightarrow r'' \rightarrow r)}$ 

:blue_square: $\quad h_x^{t+1,(0)} = U^{t}(h_x^{t,(0)}, m_x^{(0)})$


#### Homology and Cohomology-Based Passing Schemes


:red_square: $\quad m_{y \rightarrow x}^{(r' \rightarrow r)} = M^t_{\mathcal{C}}(h_{x}^{t,(r)}, h_y^{t,(r')}, x, y)$ 

:red_square: $\quad m_{y \rightarrow x}^{(r'' \rightarrow r)}  = M^t_{\mathcal{B}}(h_{x}^{t,(r)}, h_y^{t,(r'')}, x, y)$ 

:orange_square: $\quad m_x^{(r' \rightarrow r)}  = AGG_{y \in \mathcal{C}(x)} m_{y \rightarrow x}^{(r' \rightarrow r)}$ 

:orange_square: $\quad m_x^{(r'' \rightarrow r)}  = AGG_{y \in \mathcal{B}(x)} m_{y \rightarrow x}^{(r'' \rightarrow r)}$ 

:green_square: $\quad m_x^{(r)}  = AGG_{\mathcal{N}\_k \in \mathcal{N}} m_x^{(k)}$ 

:blue_square: $\quad h_{x}^{t+1,(r)} = U^{t,(r)}(h_{x}^{t,(r)}, m_{x}^{(r)})$



#### <a href="#roddenberry2022signal">[4]</a>
 
#### Convolutional Neural Networks for k-chains


:red_square: $\quad m_{y \rightarrow x}^{(r \rightarrow r)} = (\sum_p w_p (H_r)^p)\_{xy} \cdot h^{t,(r)}\_y \cdot \Theta^t$ 

:orange_square: $\quad m_x^{(r \rightarrow r)} = \sum_{y \in (\mathcal{L}\_{\uparrow}+ \mathcal{L}\_{\downarrow})(x)} m_{y \rightarrow x}^{(r \rightarrow r)}$ 

:green_square: $\quad m_x^{(r)} = m_x^{(r \rightarrow r)}$ 

:blue_square: $\quad h_x^{t+1} = \sigma(m_{x}^{(r)})$


#### Separate weightings for up and down Laplacian


:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(1 \rightarrow 0 \rightarrow 1)} = L_{\downarrow,1} \cdot h_y^{t,(1)} \cdot \Theta^{t,(1 \rightarrow 0 \rightarrow 1)}$ 

:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(1 \rightarrow 2 \rightarrow 1)} = L_{\uparrow,1} \cdot h_y^{t,(1)} \cdot \Theta^{t,(1 \rightarrow 2 \rightarrow 1)}$ 

:red_square: $\quad m_{x \rightarrow x}^{(1 \rightarrow 1)}  = h_x^{t,(1)} \cdot \Theta^{t,(1 \rightarrow 1)}$ 

:orange_square: $\quad m_x^{(1 \rightarrow 0 \rightarrow 1)}  = \sum_{y \in \mathcal{B}(x)} m_{y \rightarrow x}^{(1 \rightarrow 0 \rightarrow 1)}$ 

:orange_square: $\quad m_x^{(1 \rightarrow 2 \rightarrow 1)} = \sum_{y \in \mathcal{C}(x)} m_{y \rightarrow x}^{(1 \rightarrow 2 \rightarrow 1)}$ 

:green_square: $\quad m_x^{(1)} = m_x^{(1 \rightarrow 0 \rightarrow 1)} + m_{x \rightarrow x}^{(1 \rightarrow 1)} +m_x^{(1 \rightarrow 2 \rightarrow 1)}$ 

:blue_square: $\quad h_x^{t+1,(1)} = \sigma(m_{x}^{(1)})$

#### Neural networks for cochains of different dimensions.


:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(r \rightarrow r'' \rightarrow r)} = L_{\downarrow,1} \cdot h_y^{t,(r)} \cdot \Theta^{t,(r \rightarrow r'' \rightarrow r)}$ 

:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(r \rightarrow r' \rightarrow r)} = L_{\uparrow,r} \cdot h_y^{t,(r)} \cdot \Theta^{t,(r \rightarrow r' \rightarrow r)}$ 

:red_square: $\quad m_{x \rightarrow x}^{(r \rightarrow r)}  = h_x^{t,(r)} \cdot \Theta^{t,(r \rightarrow r)}$ 

:red_square: $\quad m_{y \rightarrow x}^{s \rightarrow r} = G^{(s \rightarrow r)} \cdot h_y^{t,(s)} \cdot \Theta^{t+1,(s \rightarrow r)}$ 

:orange_square: $\quad m_x^{(r \rightarrow r'' \rightarrow r)}  = \sum_{y \in \mathcal{B}(x)} m_{y \rightarrow x}^{(r \rightarrow r'' \rightarrow r)}$ 

:orange_square: $\quad m_x^{(r \rightarrow r' \rightarrow r)} = \sum_{y \in \mathcal{C}(x)} m_{y \rightarrow x}^{r \rightarrow r' \rightarrow r}$ 

:orange_square: $\quad m_x^{(s \rightarrow r)} = \sum_{y \in \mathcal{N}(x)} m_{y \rightarrow x}^{(s \rightarrow r)}$ 

:green_square: $\quad m_x^{(r)} = m_x^{(r \rightarrow r" \rightarrow r)} + m_{y \rightarrow x}^{(r \rightarrow r)} +m_x^{(r \rightarrow r' \rightarrow r)} + m_x^{(s \rightarrow r)}$ 

:blue_square: $\quad h_x^{t+1,(r)} = \sigma(m_{x}^{(r)})$

# Graphical illustrations

We can make graphical illustrations, called tensor diagrams, from these equations, as outlined in Section 2.3.2 of the paper.
![Screen Shot 2023-04-14 at 5 56 03 PM](https://user-images.githubusercontent.com/8267869/232175156-e0b4231d-cc27-4d58-99e5-b95cf6f9060a.png)

We use them to describe each TNN (Fig. 10 of the paper), allowing even the most complex architectures in a largely unexplored domain to be compared with other models from different domains.

## References
1. <a id="bodnar2021weisfeiler"></a>Cristian Bodnar, Fabrizio Frasca, Nina Otter, Yuguang Wang, Pietro Lio, Guido F Montufar and Michael Bronstein. Weisfeiler and Lehman Go Cellular: CW Networks. Advances in Neural Information Processing Systems. 2021
2. <a id="giusti2022cell"></a>Lorenzo Giusti, Claudio Battiloro, Lucia Testa, Paolo Di Lorenzo, Stefania Sardellitti and Sergio Barbarossa. Cell attention networks. arXiv preprint arXiv:2209.08179. 2022
3. <a id="hajij2020cell"></a>Mustafa Hajij, Kyle Istvan and Ghada Zamzmi. Cell Complex Neural Networks. NeurIPS 2020 Workshop TDA and Beyond. 2020
4. <a id="roddenberry2022signal"></a>T Mitchell Roddenberry, Michael T Schaub and Mustafa Hajij. Signal processing on cell complexes. ICASSP 2022-2022 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP). 2022
