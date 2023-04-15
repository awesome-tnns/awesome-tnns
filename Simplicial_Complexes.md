
# Schemes in the Simplicial Complex Domain

#### Message Passing Simplicial Network (MPSN), <a href="#bodnar2021topological">[4]</a>

#### MPSN (general)

:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(r \rightarrow r' \rightarrow r)} =M(h_x^{t,(r)}, h_y^{t,(r)}, h_{z}^{t, (r')}, x, y,{\Theta}^t) \qquad \text{where } r'' < r < r'$

:red_square: $\quad m_{y \rightarrow {z} \rightarrow x}^{(r \rightarrow r'' \rightarrow r)} =M(h_x^{t,(r)}, h_y^{t,(r)}, h_{z}^{t, (r'')}, x, y,{\Theta}^t)$

:red_square: $\quad m_{y \rightarrow x}^{(r' \rightarrow r)} =M(h_x^{t,(r)}, h_y^{t,(r')}, x, y, \Theta^t)$

:red_square: $\quad m_{y \rightarrow x}^{(r''\rightarrow r)} =M(h_x^{t,(r)}, h_y^{t,(r'')}, x, y, \Theta^t) $

:orange_square: $\quad m_{x}^{(r'' \rightarrow r)} =\mathrm{AGG}\_{y \in \mathcal{B}(x)}(m_{y \rightarrow x}^{(r''\rightarrow r)})$

:orange_square: $\quad m_{x}^{(r' \rightarrow r)} =\mathrm{AGG}\_{y \in \mathcal{C}(x)}(m_{y \rightarrow x}^{(r'\rightarrow r)})$

:orange_square: $\quad m_{x}^{(r \rightarrow r' \rightarrow r)}  =\mathrm{AGG}\_{y \in \mathcal{L}\uparrow(x)}(m_{y \rightarrow {z} \rightarrow x}^{(r \rightarrow r' \rightarrow r)})$

:orange_square: $\quad m_{x}^{(r \rightarrow r'' \rightarrow r)} =\mathrm{AGG}\_{y \in \mathcal{L}\downarrow(x)}(m_{y \rightarrow {z} \rightarrow x}^{(r \rightarrow r'' \rightarrow r)})$

:green_square: $\quad m_x^{(r)} = \mathrm{AGG}\_{\mathcal{N}\_k \in \mathcal{N}}(m_x^{(k)})$

:blue_square: $\quad h_x^{t+1} = \sigma (m_x^{(r)})$



#### MPSN

:red_square: $\quad m^{(r \rightarrow 1)}\_{y \rightarrow x} = (G_r^{(r \rightarrow 1)})\_{xy} \cdot h_{y}^{t,(r)} \cdot \Theta^{t,(r \rightarrow 1)} \quad \text{for } r=0,1,2$

:orange_square: $\quad m_x^{(0 \rightarrow 1)}  = \sum_{y \in \mathcal{B}(x)} m_{y \rightarrow x}^{(0 \rightarrow 1)}$

:orange_square: $\quad m_x^{(1 \rightarrow 1)} = \sum_{y \in \mathcal{L}(x)} m_{y \rightarrow x}^{(1 \rightarrow 1)}$

:orange_square: $\quad m_x^{(2 \rightarrow 1)}  = \sum_{y \in \mathcal{C}(x)} m_{y \rightarrow x}^{(2 \rightarrow 1)}$

:green_square: $\quad m_x^{(1)} = m^{(0 \rightarrow 1)}\_x + m^{(1 \rightarrow 1)}_x + m^{(2 \rightarrow 1)}x$

:blue_square: $\quad h_x^{t+1, (1)} = \sigma(m{x}^{(1)})$



#### Simplicial 2-complex convolution, <a href="#bunch2020simplicial">[5]</a>


:red_square: $\quad m_{y\rightarrow x}^{(0\rightarrow 0)} = ({\tilde{A}\_{\uparrow,0}})\_{xy} \cdot h_y^{t,(0)} \cdot \Theta^{t,(0\rightarrow0)}$

:red_square: $\quad m^{(1\rightarrow0)}\_{y\rightarrow x}  = (B_1)\_{xy} \cdot h_y^{t,(0)} \cdot \Theta^{t,(1\rightarrow 0)}$

:red_square: $\quad m^{(0 \rightarrow 1)}\_{y \rightarrow x}  = (\tilde B_1)\_{xy} \cdot h_y^{t,(0)} \cdot \Theta^{t,(0 \rightarrow1)}$

:red_square: $\quad m^{(1\rightarrow1)}\_{y\rightarrow x} = ({\tilde{A}\_{\downarrow,1}} + {\tilde{A}\_{\uparrow,1}})\_{xy} \cdot h_y^{t,(1)} \cdot \Theta^{t,(1\rightarrow1)}$

:red_square: $\quad m^{(2\rightarrow1)}\_{y \rightarrow x}  = (B_2)\_{xy} \cdot h_y^{t,(2)} \cdot \Theta^{t,(2 \rightarrow1)}$

:red_square: $\quad m^{(1 \rightarrow 2)}\_{y \rightarrow x}  = (\tilde B_2)\_{xy} \cdot h_y^{t,(1)} \cdot \Theta^{t,(1 \rightarrow 2)}$

:red_square: $\quad m^{(2 \rightarrow 2)}\_{y \rightarrow x}  = ({\tilde{A}\_{\downarrow,2}})\_{xy} \cdot h_y^{t,(2)} \cdot \Theta^{t,(2 \rightarrow 2)}$

:orange_square: $\quad m_x^{(0 \rightarrow 0)}  = \sum_{y \in \mathcal{L}\_\uparrow(x)} m_{y \rightarrow x}^{(0 \rightarrow 0)}$

:orange_square: $\quad m_x^{(1 \rightarrow 0)}  = \sum_{y \in \mathcal{C}(x)} m_{y \rightarrow x}^{(1 \rightarrow 0)}$

:orange_square: $\quad m_x^{(0 \rightarrow 1)}  = \sum_{y \in \mathcal{B}(x)} m_{y \rightarrow x}^{(0 \rightarrow 1)}$

:orange_square: $\quad m_x^{(1 \rightarrow 1)}  = \sum_{y \in (\mathcal{L}\_\uparrow(x) + \mathcal{L}\_\downarrow(x))} m_{y \rightarrow x}^{(1 \rightarrow 1)}$

:orange_square: $\quad m_x^{(2 \rightarrow 1)} = \sum_{y \in \mathcal{C}(x)} m_{y \rightarrow x}^{(2 \rightarrow 1)}$

:orange_square: $\quad m_x^{(1 \rightarrow 2)}  = \sum_{y \in \mathcal{B}(x)} m_{y \rightarrow x}^{(1 \rightarrow 2)}$

:orange_square: $\quad m_x^{(2 \rightarrow 2)}  = \sum_{y \in \mathcal{L}\_\downarrow(x)} m_{y \rightarrow x}^{(2 \rightarrow 2)}$

:green_square: $\quad m_x^{(0)}  = m_x^{(1\rightarrow0)}+ m_x^{(0\rightarrow0)}$

:green_square: $\quad m_x^{(1)}  = m_x^{(2\rightarrow1)}+ m_x^{(1\rightarrow1)}$

:blue_square: $\quad h^{t+1, (0)}\_x  = \sigma(m_x^{(0)})$

:blue_square: $\quad h^{t+1, (1)}\_x  = \sigma(m_x^{(1)})$

:blue_square: $\quad h^{t+1, (2)}\_x  = \sigma(m_x^{(2)})$


#### Block Simplicial Complex Neural Networks (BScNets), <a href="#chen2022bscnets">[19]</a>


:red_square: $\quad m_{y \rightarrow x}^{(r \rightarrow r)} = (H_r)\_{xy} \cdot h_{{y}}^{t, (r)} \cdot \Theta^{t,(r \rightarrow r)}$

:red_square: $\quad m_{y \rightarrow x}^{(r \rightarrow r')} = (G_{r \rightarrow r'})\_{xy} \cdot h^{t, (r)}\_y \cdot \Theta^{t,(r \rightarrow r')}$

:red_square: $\quad m_{y \rightarrow x}^{(r' \rightarrow r)} = (G{r' \rightarrow r})\_{xy} \cdot h_y^{t,(r')} \cdot \Theta^{t,(r' \rightarrow r)}$

:red_square: $\quad m_{y \rightarrow x}^{(r' \rightarrow r')}  = (H_{r'})\_{xy} \cdot h_{{y}}^{t,(r')} \cdot \Theta^{t,(r' \rightarrow r')}$

:orange_square: $\quad m_x^{(r' \rightarrow r)} = \sum_{y \in \mathcal{N}\_\uparrow(x)} m_{y \rightarrow x}^{(r' \rightarrow r)}$

:orange_square: $\quad m_x^{(r \rightarrow r')}  = \sum_{y \in \mathcal{N}\_\downarrow(x)} m_{y \rightarrow x}^{(r \rightarrow r')}$

:orange_square: $\quad m_x^{(r \rightarrow r)}  = \sum_{y \in (\mathcal{L}\_\uparrow+\mathcal{L}\_\downarrow)(x)} m_{y \rightarrow x}^{(r \rightarrow r)}$

:orange_square: $\quad m_x^{(r' \rightarrow r')}  = \sum_{y \in (\mathcal{L}\_\uparrow+\mathcal{L}\_\downarrow)(x)} m_{y \rightarrow x}^{(r' \rightarrow r')}$

:green_square: $\quad m_x^{(r)} = m_x^{(r \rightarrow r)}+ m_x^{(r' \rightarrow r)}$

:green_square: $\quad m_x^{(r')}  = m_x^{(r' \rightarrow r')} + m_x^{(r \rightarrow r')}$

:blue_square: $\quad h^{t+1, (r)}\_x  = \sigma(m_x^{(r)})$

:blue_square: $\quad h^{t+1, (r')}\_x = \sigma(m_x^{(r')})$


#### Simplicial Neural Networks, <a href="#ebli2020simplicial">[16]</a>


:red_square: $\quad m_{y \rightarrow x}^{p, (0 \rightarrow 0)} = ((L_{\uparrow,0})^p)\_{xy} \cdot h_y^{t,(0)} \cdot \Theta^{t,p}$

:red_square: $\quad m_{y \rightarrow x}^{p, (1 \rightarrow 1)}  = ((H_{1})^p)\_{xy} \cdot h_y^{t,(1)} \cdot \Theta^{t,p}$

:red_square: $\quad m_{y \rightarrow x}^{p, (2 \rightarrow 2)}  = ((L_{\downarrow,2})^p)\_{xy} \cdot h_y^{t,(2)} \cdot \Theta^{t,p}$

:orange_square: $\quad m_{x}^{p, (0 \rightarrow 0)}  = \sum_{y \in \mathcal{L}\_\uparrow(x)} m_{y \rightarrow x}^{p, (0 \rightarrow 0)}$

:orange_square: $\quad m_{x}^{p, (1 \rightarrow 1)}  = \sum_{y \in (\mathcal{L}\_\uparrow + \mathcal{L}\_\downarrow)(x)} m_{y \rightarrow x}^{p, (1 \rightarrow 1)}$

:orange_square: $\quad m_{x}^{p, (2 \rightarrow 2)}  = \sum_{y \in \mathcal{L}\_\downarrow(x)} m_{y \rightarrow x}^{p, (2 \rightarrow 2)}$

:orange_square: $\quad m_x^{(0 \rightarrow 0)}  = \sum_{p=1}^{P_0} (m_{x}^{p,(0 \rightarrow 0)})^{p}$

:orange_square: $\quad m_x^{(1 \rightarrow 1)}  = \sum_{p=1}^{P_1} (m_{x}^{p,(1 \rightarrow 1)})^{p}$

:orange_square: $\quad m_x^{(2 \rightarrow 2)}  = \sum_{p=1}^{P_2} (m_{x}^{p,(2 \rightarrow 2)})^{p}$

:green_square: $\quad m_x^{(0)}  = m_x^{(0 \rightarrow 0)}$

:green_square: $\quad m_x^{(1)}  = m_x^{(1 \rightarrow 1)}$

:green_square: $\quad m_x^{(2)}  = m_x^{(2 \rightarrow 2)}$

:blue_square: $\quad h_x^{t+1, (0)}  = \sigma (m_{x}^{(0)})$

:blue_square: $\quad h_x^{t+1, (1)}  = \sigma (m_{x}^{(1)})$

:blue_square: $\quad h_x^{t+1, (2)}  = \sigma (m_{x}^{(2)})$


#### Simplicial Attention Network (SAN), <a href="#giusti2022simplicial">[7]</a>


:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{u,(1 \rightarrow 2 \rightarrow 1)}  = ((L_{\uparrow,1} \odot \operatorname{att}(h_z^{t,(2)}, h_y^{t,(1)}))^u)\_{xy} \cdot h_y^{t,(1)} \cdot \Theta^{t,u}$

:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{d,(1 \rightarrow 0 \rightarrow 1)}  = ((L_{\downarrow,1} \odot \operatorname{att}(h_z^{t,(0)}, h_y^{t,(1)}))^d)\_{xy} \cdot h_y^{t,(1)} \cdot \Theta^{t,d}$

:red_square: $\quad m^{p,(1 \rightarrow 1)}\_{y \rightarrow x} = ((1-wH_1)^p)\_{xy} \cdot h_y^{t,(1)} \cdot \Theta^{t,p}$

:orange_square: $\quad m_{x}^{u,(1 \rightarrow 2 \rightarrow 1)}  = \sum_{y \in \mathcal{L}\_\uparrow(x)} m_{y \rightarrow \{z\} \rightarrow x}^{u,(1 \rightarrow 2 \rightarrow 1)}$

:orange_square: $\quad m_{x}^{d,(1 \rightarrow 0 \rightarrow 1)}  = \sum_{y \in \mathcal{L}\downarrow(X)} m_{y \rightarrow \{z\} \rightarrow x}^{d,(1 \rightarrow 0 \rightarrow 1)}$

:orange_square: $\quad m^{p,(1 \rightarrow 1)}\_{x}  = m^{p,(1 \rightarrow 1)}\_{x \rightarrow x}$

:green_square: $\quad m_x^{(1)}  = \sum_{p=1}^P m_x^{p,(1 \rightarrow 1)} + \sum_{u=1}^{U} m_{x}^{u,(1 \rightarrow 2 \rightarrow 1)} + \sum_{d=1}^{D} m_{x}^{d,(1 \rightarrow 0 \rightarrow 1)}$

:blue_square: $\quad h_x^{t+1, (1)} = \sigma(m_x^{(1)})$


#### Simplicial Attention Network (SAT), <a href="#goh2022simplicial">[2]</a>


:red_square: $\quad m_{y \rightarrow x}^{(r-1 \rightarrow r)} = (B_{r}^T\cdot \text{att}(h_{y \in \mathcal{B}(x)}^{t,(r-1)},h_x^{t,(r)}))\_{xy} \cdot h_y^{t,(r-1)} \cdot \Theta^{t,(r-1 \rightarrow r)}$

:red_square: $\quad m_{y \rightarrow x}^{(r+1 \rightarrow r)}  = (B_{r+1}\cdot \text{att}(h_{y \in \mathcal{C}(x)}^{t,(r+1)},h_x^{t,(r)}))\_{xy} \cdot h_y^{t,(r+1)} \cdot \Theta^{t,(r+1 \rightarrow r)}$

:orange_square: $\quad m_{x}^{(r-1 \rightarrow r)} =\sum_{y \in \mathcal{B}(x)} m_{y \rightarrow x}^{(r-1 \rightarrow r)}$

:orange_square: $\quad m_{x}^{(r+1 \rightarrow r)}  =\sum_{y \in \mathcal{C}(x)} m_{y \rightarrow x}^{(r+1 \rightarrow r)}$

:green_square: $\quad m_x^{(r)}  = \text{AGG}\_{\mathcal{N}\_k \in \mathcal{N}} m_{y \rightarrow x}^{\mathcal{N}}$

:blue_square: $\quad h_x^{t+1, (r)}  = \sigma(m_x^{(r)})$


#### High Skip Network <a href="#hajij2022high">[12]</a>

#### For link prediction


:red_square: $\quad m_{{y \rightarrow z}}^{(0 \rightarrow 0)} = \sigma ((A_{\uparrow,0})\_{xy} \cdot h^{t,(0)}\_y \cdot \Theta^{t,(0)1})$

:red_square: $\quad m_{z \rightarrow x}^{(0 \rightarrow 0)}  = (A_{\uparrow,0})\_{xy} \cdot m_{y \rightarrow z}^{(0 \rightarrow 0)} \cdot \Theta^{t,(0)2}$

:red_square: $\quad m_{{y \rightarrow z}}^{(0 \rightarrow 1)}  = \sigma((B_1^T)\_{zy} \cdot h_y^{t,(0)} \cdot \Theta^{t,(0 \rightarrow 1)})$

:red_square: $\quad m_{z \rightarrow x)}^{(1 \rightarrow 0)}  = (B_1)\_{xz} \cdot m_{z \rightarrow x}^{(0 \rightarrow 1)} \cdot \Theta^{t, (1 \rightarrow 0)}$

:orange_square: $\quad m_{x}^{(0 \rightarrow 0)}  = \sum_{z \in \mathcal{L}\_\uparrow(x)} m_{z \rightarrow x}^{(0 \rightarrow 0)}$

:orange_square: $\quad m_{x}^{(1 \rightarrow 0)}  = \sum_{z \in \mathcal{C}(x)} m_{z \rightarrow x}^{(1 \rightarrow 0)}$

:green_square: $\quad m_x^{(0)}  = m_x^{(0 \rightarrow 0)} + m_x^{(1 \rightarrow 0)}$

:blue_square: $\quad h_x^{t+1,(0)}  = I(m_x^{(0)})$


#### For node classification


:red_square: $\quad m_{z \rightarrow x}^{(0 \rightarrow 0) \in \text{seq1}} = (A_{\uparrow,0})\_{xz} \cdot m_{y \rightarrow z}^{(0 \rightarrow 0)\in \text{seq1}} \cdot \Theta^{t,1}$

:red_square: $\quad m_{y \rightarrow z}^{(0 \rightarrow 1) \in \text{seq2}}  = (B_1^T)\_{zy} \cdot h_y^{t,(0)} \cdot \Theta^{t,0}$

:red_square: $\quad m_{z \rightarrow u}^{(1 \rightarrow 1)1 \in \text{seq2}}  = \sigma((A{\uparrow,1})\_{uz} \cdot m_{y \rightarrow z}^{(0 \rightarrow 1) \in \text{seq2}} \cdot \Theta^{t,i,1})$

:red_square: $\quad m_{u \rightarrow v}^{(1 \rightarrow 1)^i_2 \in \text{seq2}} = \sigma((A_{\uparrow,1})\_{vu} \cdot m_{z \rightarrow u}^{(1 \rightarrow 1) \in \text{seq2}} \cdot \Theta_{t,i,1})$

:red_square: $\quad m_{v \rightarrow w}^{(1 \rightarrow 1)^i_2 \in \text{seq2}}  = \sigma((A_{\uparrow,0})\_{wv} \cdot m_{u \rightarrow v}^{(1 \rightarrow 1)^i_2 \in \text{seq2}} \cdot \Theta_{t,i,2})$

:red_square: $\quad m_{w \rightarrow s}^{(1 \rightarrow 0)\in \text{seq2}} = (B_1)\_{sw} \cdot m_{v \rightarrow w}^{(1 \rightarrow 1)\_2^d \in \text{seq2}} \cdot \Theta^t$

:red_square: $\quad m_{s \rightarrow x}^{(0 \rightarrow 0) \in \text{seq2}}  = (A_{\uparrow,0})\_{xs} \cdot m_{w \rightarrow s}^{(1 \rightarrow 0)\in \text{seq2}} \cdot \Theta^t$

:red_square: $\quad m_{y \rightarrow z}^{(0 \rightarrow 1) \in \text{seq3}} = (B_1^T)\_{zy} \cdot h_y^{t,(0)} \cdot \Theta^{t,0}$

:red_square: $\quad m_{z \rightarrow z}^{(1)^i \in \text{seq3}}  = m_{z \rightarrow z}^{(0,1) \text{ or } (1)^{i-1} \in \text{seq3}}$

:red_square: $\quad m_{z \rightarrow w}^{(1 \rightarrow 0) \in \text{seq3}}  = (B_1)\_{wz} \cdot m_{y \rightarrow z}^{(1)^{d} \in \text{seq3}} \cdot \Theta^t$

:red_square: $\quad m_{w \rightarrow x}^{(0 \rightarrow 0)\in \text{seq3}}  = (A_{\uparrow,0})\_{xw} \cdot m_{z \rightarrow w}^{(1 \rightarrow 0) \in \text{seq3}} \cdot \Theta^t$

:orange_square: $\quad m_{x}^{\text{seq1},(0)}  = \sum_{z \in \mathcal{L}\_\uparrow(x)} m_{z \rightarrow x}^{(0 \rightarrow 0) \in \text{seq1}}$

:orange_square: $\quad m_{x}^{\text{seq2},(0)} = \sum_{s \in \mathcal{L}\_\uparrow(x)} m_{s \rightarrow x}^{(0 \rightarrow 0) \in \text{seq2}}$

:orange_square: $\quad m_{x}^{\text{seq3},(0)} = \sum_{w \in \mathcal{L}\_\uparrow(x)} m_{w \rightarrow x}^{(0 \rightarrow 0) \in \text{seq3}}$

:green_square: $\quad m_x^{(0)} = m_x^{\text{seq1},(0)} + m_x^{\text{seq2},(0)} + m_x^{\text{seq3},(0)}$

:blue_square: $\quad h_x^{t+1,(0)} = I(m_x^{(0)})$


#### For vector embedding


:red_square: $\quad m_{{y \rightarrow z}}^{(1 \rightarrow 0) \in \text{seq1}}  = \sigma((B_1)\_{zy} \cdot h_y^{t,(0)} \cdot \Theta^{t,(1 \rightarrow 0)})$

:red_square: $\quad m_{{y \rightarrow z}}^{(1 \rightarrow 1) \in \text{seq2}} = \sigma ((\tilde A_{\uparrow, 1})\_{zy} \cdot h_y^{t,(0)} \cdot \Theta^{t,(1 \rightarrow 1)})$

:red_square: $\quad m_{{y \rightarrow z}}^{(1 \rightarrow 2) \in \text{seq3}}  = \sigma ((B^T_2)\_{zy} \cdot h^{t,(0)}\_y \cdot \Theta^{t,(1 \rightarrow 2)})$

:red_square: $\quad m_{z \rightarrow x}^{(0,1) \in \text{seq1}}  = (B_1^T)\_{xz} \cdot m_{y \rightarrow z}^{(1 \rightarrow 0) \in \text{seq1}} \cdot \Theta^{t,(0 \rightarrow 1)})$

:red_square: $\quad m_{z \rightarrow x}^{(1 \rightarrow 1) \in \text{seq2}} = (\tilde A_{\uparrow, 1})\_{xz} \cdot m_{y \rightarrow z}^{(1 \rightarrow 1) \in \text{seq2}} \cdot \Theta^{t,(1 \rightarrow 1)}$

:red_square: $\quad m_{z \rightarrow x}^{(2 \rightarrow 1) \in \text{seq3}} = (B_2)\_{xz} \cdot m_{y \rightarrow z}^{(1 \rightarrow 2) \in \text{seq3}} \cdot \Theta^{t,(2 \rightarrow 1)}$

:orange_square: $\quad m_{x}^{\text{seq1},(1)}  = \sum_{z \in \mathcal{B}(x)} m_{z \rightarrow x}^{(0 \rightarrow 1) \in \text{seq1}}$

:orange_square: $\quad m_{x}^{\text{seq2},(1)}  = \sum_{z \in \mathcal{L}\_\uparrow(x)} m_{z \rightarrow x}^{(1 \rightarrow 1) \in \text{seq2}}$

:orange_square: $\quad m_{x}^{\text{seq3},(1)}  = \sum_{z \in \mathcal{C}(x)} m_{z \rightarrow x}^{(2 \rightarrow 1) \in \text{seq3}}$

:green_square: $\quad m_x^{(1)}  = m_x^{\text{seq1},(1)} + m_x^{\text{seq2},(1)} + m_x^{\text{seq3},(1)}$

:blue_square: $\quad h_x^{t+1,(1)} = I(m_x^{(1)})$



#### Simplicial Complex Autoencoder, <a href="#hajij2022simplicial">[11]</a>

#### Adjacency Message Passing Scheme

:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(r \rightarrow r' \rightarrow r)}  = M(h_{x}^{t, (r)}, h_{y}^{t, (r)}, h_{y}^{t, (r)}), x, y, \Theta^t) \qquad \text{where } r'' < r < r'$

:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(r' \rightarrow r)} = M(h_{x}^{t, (r)}, h_{y}^{t, (r')}, h_{y}^{t, (r')}), x, y, \Theta^t)$

:orange_square: $\quad m_x^{(r \rightarrow r' \rightarrow r)}  = \text{AGG}\_{y \in \mathcal{L}\_\uparrow(x)} m_{y \rightarrow \{z\} \rightarrow x}^{(r \rightarrow r' \rightarrow r)}$

:orange_square: $\quad m_x^{(r' \rightarrow r)} = \text{AGG}\_{y \in \mathcal{C}(x)} m_{y \rightarrow \{z\} \rightarrow x}^{(r' \rightarrow r)}$

:green_square: $\quad m_x^{(r)}  = \text{AGG}\_{\mathcal{N}\_k \in \mathcal{N}}(m_x^{(k)})$

:blue_square: $\quad h_{x}^{t+1, (r)} = U(h_x^{t, (r)}, m_{x}^{(r)})$

#### Coadjacency Message Passing Scheme

:red_square: $\quad m_{y \rightarrow x}^{(r \rightarrow r'' \rightarrow r)} = M(h_{x}^{t, (r)}, h_{y}^{t, (r)},att(h_{x}^{t, (r)}, h_{y}^{t, (r)}),x,y,{\Theta^t}) \qquad \text{where } r'' < r < r'$

:red_square: $\quad m_{y \rightarrow x}^{(r'' \rightarrow r)} = M(h_{x}^{t, (r)}, h_{y}^{t, (r'')},att(h_{x}^{t, (r)}, h_{y}^{t, (r'')}),x,y,{\Theta^t})$

:orange_square: $\quad m_x^{(r \rightarrow r)}  = AGG_{y \in \mathcal{L}\_\downarrow(x)} m_{y \rightarrow x}^{(r \rightarrow r)}$

:orange_square: $\quad m_x^{(r'' \rightarrow r)} = AGG_{y \in \mathcal{B}(x)} m_{y \rightarrow x}^{(r'' \rightarrow r)}$

:green_square: $\quad m_x^{(r)} = AGG_{\mathcal{N}\_k \in \mathcal{N}}(m_x^{(k)})$

:blue_square: $\quad h_{x}^{t+1, (r)} = U(h_x^{t, (r)}, m_{x}^{(r)})$


#### Homology and Cohomology Message Passing Scheme

:red_square: $\quad m_{y \rightarrow x}^{(r' \rightarrow r)}  = M(h_{x}^{t, (r)}, h_{y}^{t, (r')},att(h_{x}^{t, (r)}, h_{y}^{t, (r')}),x,y,{\Theta^t}) \qquad \text{where } r'' < r < r'$

:red_square: $\quad m_{y \rightarrow x}^{(r'' \rightarrow r)} = M(h_{x}^{t, (r)}, h_{y}^{t, (r'')},att(h_{x}^{t, (r)}, h_{y}^{t, (r'')}),x,y,{\Theta^t})$

:orange_square: $\quad m_x^{(r' \rightarrow r)} = AGG_{y \in \mathcal{C}(x)} m_{y \rightarrow x}^{(r' \rightarrow r)}$

:orange_square: $\quad m_x^{(r'' \rightarrow r)}  = AGG_{y \in \mathcal{B}(x)} m_{y \rightarrow x}^{(r'' \rightarrow r)}$

:green_square: $\quad m_x^{(r)}  = AGG_{\mathcal{N}\_k \in \mathcal{N}}(m_x^{(k)})$

:blue_square: $\quad h_{x}^{t+1, (r)} = U(h_x^{t, (r)}, m_{x}^{(r)})$



#### Dist2Cycle, <a href="#keros2022dist2cycle">[1]</a>

:red_square: $\quad m^{(1 \rightarrow 1)}\_{y \rightarrow x}  = (A \odot (I + L\downarrow)^+{xy}) \cdot h_{y}^{t,(1)}\cdot \Theta^t$

:orange_square: $\quad m_x^{(1 \rightarrow 1)}  = \sum_{y \in \mathcal{L}\_\downarrow(x)} m_{y \rightarrow x}^{(1 \rightarrow 1)}$

:green_square: $\quad m_x^{(1)}  = m^{(1 \rightarrow 1)}_x$

:blue_square: $\quad h_x^{t+1,(1)} = \sigma(m_{x}^{(1)})$


#### Simplicial Graph Attention Network, <a href="#lee2022sgatsg">[15]</a>


:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(r \rightarrow r+1 \rightarrow r)} = (\tilde A_{\uparrow,r}\cdot att(h_y^{t,(r)},h_{z \in \mathcal{C}(x)}^{t,(r+1)},h_x^{t,(r)}))\_{xy} \cdot h_y^{t,(r-1)} \cdot \Theta^{t,(r+1 \rightarrow r)})$

:orange_square: $\quad m_{x}^{(r \rightarrow r+1 \rightarrow r)}  = \sum_{y \in \mathcal{L_\uparrow}(x)} m_{y \rightarrow \{z\} \rightarrow x}^{(r \rightarrow r+1 \rightarrow r)}$

:green_square: $\quad m_x^{(r)} = m_{x}^{(r \rightarrow r+1 \rightarrow r)}$

:blue_square: $\quad h_x^{t+1, (r)}  = \sigma(m_x^{(r)})$


#### Simplicial Complex Net (SCoNe), <a href="#roddenberryglaze2021principled">[18]</a>


:red_square: $\quad m^{(1 \rightarrow 0 \rightarrow 1)}\_{y \rightarrow \{z\} \rightarrow x}  = (L_{\downarrow,1})\_{xy} \cdot h_y^{t,(1)} \cdot \Theta^{t,(1 \rightarrow 0 \rightarrow 1)}$

:red_square: $\quad m_{x \rightarrow x}^{(1 \rightarrow 1)}  = h_x^{t,(1)} \cdot \Theta^{t,(1 \rightarrow 1)}$

:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(1 \rightarrow 2 \rightarrow 1)}  = (L_{\uparrow,1})\_{xy} \cdot h_y^{t,(1)} \cdot \Theta^{t,(1 \rightarrow 2 \rightarrow 1)}$

:orange_square: $\quad m_{x}^{(1 \rightarrow 0 \rightarrow 1)} = \sum_{y \in \mathcal{L}\_\downarrow(x)} m_{y \rightarrow \{z\} \rightarrow x}^{(1 \rightarrow 0 \rightarrow 1)}$

:orange_square: $\quad m_{x}^{(1 \rightarrow 2 \rightarrow 1)}  = \sum_{y \in \mathcal{L}\_\uparrow(x)} m_{y \rightarrow \{z\} \rightarrow x}^{(1 \rightarrow 2 \rightarrow 1)}$

:green_square: $\quad m_x^{(1)}  = m_{x}^{(1 \rightarrow 0 \rightarrow 1)} + m_{x \rightarrow x}^{(1 \rightarrow 1)} + m_{x}^{(1 \rightarrow 2 \rightarrow 1)}$

:blue_square: $\quad h_x^{t,(1)} = \sigma(m_x^{(1)})$


#### Simplicial Convolutional Neural Networks (SCNN) <a href="#yang2022simplicial">[9]</a>

Here, $\alpha$ coefficients are determined by solving the least-squares problem defined in <a href="#schaub2021signal">[10]</a>.


:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{p,u,(1 \rightarrow 2 \rightarrow 1)}  = ((L_{\uparrow,1})^u)\_{xy} \cdot h_y^{t,(1)} \cdot (\alpha^{t, p, u} \cdot I)$

:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{p,d,(1 \rightarrow 0 \rightarrow 1)} = ((L_{\downarrow,1})^d)\_{xy} \cdot h_y^{t,(1)} \cdot (\alpha^{t, p, d} \cdot I)$

:red_square: $\quad m^{(1 \rightarrow 1)}\_{x \rightarrow x} = \alpha \cdot h_x^{t, (1)}$

:orange_square: $\quad m_{x}^{p,u,(1 \rightarrow 2 \rightarrow 1)}  = \sum_{y \in \mathcal{L}\_\uparrow(X)}m_{y \rightarrow \{z\} \rightarrow x}^{p,u,(1 \rightarrow 2 \rightarrow 1)}$

:orange_square: $\quad m_{x}^{p,d,(1 \rightarrow 0 \rightarrow 1)} = \sum_{y \in \mathcal{L}\_\downarrow(X)}m_{y \rightarrow \{z\} \rightarrow x}^{p,d,(1 \rightarrow 0 \rightarrow 1)}$

:orange_square: $\quad m^{(1 \rightarrow 1)}\_{x} = m^{(1 \rightarrow 1)}\_{x \rightarrow x}$

:green_square: $\quad m_x^{(1)}  = m_x^{(1 \rightarrow 1)} + \sum_{p=1}^P( \sum_{u=1}^{U} m_{x}^{p,u,(1 \rightarrow 2 \rightarrow 1)} + \sum_{d=1}^{D} m_{x}^{p,d,(1 \rightarrow 0 \rightarrow 1)})$

:blue_square: $\quad h_x^{t+1, (1)} = \sigma(m_x^{(1)})$


#### Simplicial Complex Convolutional Neural Network (SCCNN) <a href="#yang2023convolutional">[8]</a>

:red_square: $\quad m_{y \rightarrow z}^{(0\rightarrow1)}  = B_1^T \cdot h_y^{t,(0)} \cdot \Theta^{t,(0 \rightarrow 1)}$

:orange_square: $\quad m_{z}^{(0\rightarrow1)}  = \frac{1}\sum_{y \in \mathcal{B}(z)} m_{y \rightarrow z}^{(0\rightarrow1)} \qquad \text{where} \sum \text{represents a mean.}$

:red_square: $\quad m_{z \rightarrow x}^{(1 \rightarrow 0)} = B_1\odot att(m_{z \in \mathcal{C}(x)}^{(0\rightarrow1)}, h_x^{t,(0)}) \cdot m_z^{(0\rightarrow1)} \cdot \Theta^{t,(1 \rightarrow 0)}$

:orange_square: $\quad m_x^{(1\rightarrow0)}  = \sum_{z \in \mathcal{C}(x)} m_{z \rightarrow x}^{(1\rightarrow0)} \qquad \text{where} \sum \text{represents a mean.}$

:green_square: $\quad m_x^{(0)}  = m_x^{(1\rightarrow0)}$

:blue_square: $\quad h_x^{t+1, (0)} = \Theta^{t, \text{update}} \cdot (h_x^{t,(0)}||m_x^{(0)})+b^{t, \text{update}}$


#### <a href="#yang2022efficient">[14]</a>

#### Simplicial Convolutional Network

:red_square: $\quad m^{(r \rightarrow r)}\_{y \rightarrow x}  = (2I + H_r)\_{{xy}} \cdot h_{y}^{t,(1)}\cdot \Theta^t$

:orange_square: $\quad m_x^{(1 \rightarrow 1)}  = \sum_{y \in (\mathcal{L}\_\downarrow+\mathcal{L}\_\uparrow)(x)} m_{y \rightarrow x}^{(1 \rightarrow 1)}$

:green_square: $\quad m_x^{(1)}  = m^{(1 \rightarrow 1)}_x$

:blue_square: $\quad h_x^{t+1,(1)} = \sigma(m_{x}^{(1)})$

#### Simplicial Complex Convolutional Network

:red_square: $\quad m^{(r \rightarrow r)}{y \rightarrow x}  = (H_r)\_{xy}\cdot h_{y}^{t,(r)}\cdot \Theta^{t,(r \rightarrow r)}$

:red_square: $\quad m^{(r-1 \rightarrow r)}\_{y \rightarrow x}  = (B_r^T)\_{xy}\cdot h_{y}^{t,(r-1)}\cdot \Theta^{t,(r-1 \rightarrow r)}$

:red_square: $\quad m^{(r+1 \rightarrow r)}\_{y \rightarrow x} = (B_{r+1})\_{xy}\cdot h{y}^{t,(r+1)}\cdot \Theta^{t,(r+1 \rightarrow r)}$

:orange_square: $\quad m_x^{(r-1 \rightarrow r)}  = \sum_{y \in \mathcal{B}(x)} m_{y \rightarrow x}^{(r-1 \rightarrow r)}$

:orange_square: $\quad m_x^{(r \rightarrow r)}  = \sum_{y \in \mathcal{L}\_r (x)} m_{y \rightarrow x}^{(r \rightarrow r)}$

:orange_square: $\quad m_x^{(r+1 \rightarrow r)}  = \sum_{y \in \mathcal{C}(x)} m_{y \rightarrow x}^{(r+1 \rightarrow r)}$

:green_square: $\quad m_x^{(r)}  = m^{(r-1 \rightarrow r)}\_x + m^{(r \rightarrow r)}\_x + m^{(r+1 \rightarrow r)}\_x$

:blue_square: $\quad h_x^{t+1, (r)} = \sigma(m_{x}^{(r)})$





\subsection{Schemes in the Cellular Complex Domain}\label{mp-cellular}


#### CW Network (CWN), <a href="#bodnar2021weisfeiler">[3]</a>


:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(r \rightarrow r' \rightarrow r)} = M_{\mathcal{L}\uparrow}(h_x^{t,(r)}, h_y^{t,(r)}, h_z^{t,(r')})$

:red_square: $\quad m_{y \rightarrow x}^{(r'' \rightarrow r)} = M_{\mathcal{B}}(h_x^{t,(r)}, h_y^{t,(r'')})$

:orange_square: $\quad m_x^{(r'' \rightarrow r)} = AGG_{y \in \mathcal{B}(x)} m_{y \rightarrow x}^{(r'' \rightarrow r)}$

:orange_square: $\quad m_x^{(r \rightarrow r' \rightarrow r)} = AGG_{y \in \mathcal{L}(x)} m_{y \rightarrow \{z\} \rightarrow x}^{(r \rightarrow r' \rightarrow r)}$

:green_square: $\quad m_x^{(r)} = AGG_{\mathcal{N}\_k \in \mathcal{N}} (m_x^k)$

:blue_square: $\quad h_x^{t+1,(r)} = U\left(h_x^{t,(r)}, m_x^{(r)}\right)$


#### Cell Attention Network (CAN), <a href="#giusti2022cell">[6]</a>


:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(1 \rightarrow 2 \rightarrow 1)} = \sigma\left((L_{\uparrow,1} \odot att(h_{y \in \mathcal{L}\uparrow(x)}^{t,(1)}, h_x^{t,(1)}))\_{xy} \cdot h_y^{t,(1)} \cdot \Theta^{t,(1 \rightarrow 2 \rightarrow 1)} \right)$

:red_square: $\quad m_{y \rightarrow \{z\} \rightarrow x}^{(1 \rightarrow 0 \rightarrow 1)} = \sigma \left((L_{\downarrow,1} \odot att(h_{y \in \mathcal{L}\downarrow(x)}^{t,(1)}, h_x^{t,(1)}))\_{xy} \cdot h_y^{t,(1)} \cdot \Theta^{t,(1 \rightarrow 0 \rightarrow 1)} \right)$

:red_square: $\quad m^{(1 \rightarrow 1)}\_{x \rightarrow x} = \sigma\left((1+\epsilon)\cdot h_x^{t, (1)} \cdot \Theta^{t,(1 \rightarrow 1)} \right)$

:orange_square: $\quad m_{x}^{(1 \rightarrow 2 \rightarrow 1)} = \sum_{y \in \mathcal{L}\_\uparrow(x)}m_{y \rightarrow \{z\} \rightarrow x}^{(1 \rightarrow 2 \rightarrow 1)}$

:orange_square: $\quad m_{x}^{(1 \rightarrow 0 \rightarrow 1)} = \sum_{y \in \mathcal{L}\_\downarrow(x)}m_{y \rightarrow \{z\} \rightarrow x}^{(1 \rightarrow 0 \rightarrow 1)}$

:orange_square: $\quad m^{(1 \rightarrow 1)}\_{x} = m^{(1 \rightarrow 1)}\_{x \rightarrow x}$

:green_square: $\quad m_x^{(1)} = m_x^{(1 \rightarrow 1)} + m_{x}^{(1 \rightarrow 2 \rightarrow 1)} + m_{x}^{(1 \rightarrow 0 \rightarrow 1)}$

:blue_square: $\quad h_x^{t+1, (1)} = \sigma(\theta_{att} \cdot m_x^{(1)})\cdot m_x^{(1)}$


#### Convolutional Cell Complex Networks (CCXN), <a href="#hajij2020cell">[13]</a>


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



#### <a href="#roddenberry2022signal">[17]</a>

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
![Screen Shot 2023-04-14 at 5 59 42 PM](https://user-images.githubusercontent.com/8267869/232175291-f79c0a47-74d3-4a6b-a514-ff51edde548c.png)

We use them to describe each TNN (Fig. 10 of the paper), allowing even the most complex architectures to be compared with other models from different domains.

## References
1. <a id="keros2022dist2cycle"></a>Alexandros D Keros, Vidit Nanda and Kartic Subr. Dist2cycle: A simplicial neural network for homology localization. Proceedings of the AAAI Conference on Artificial Intelligence. 2022
2. <a id="goh2022simplicial"></a>Christopher Wei Jin Goh, Cristian Bodnar and Pietro Lio. Simplicial attention networks. arXiv preprint arXiv:2204.09455. 2022
3. <a id="bodnar2021weisfeiler"></a>Cristian Bodnar, Fabrizio Frasca, Nina Otter, Yuguang Wang, Pietro Lio, Guido F Montufar and Michael Bronstein. Weisfeiler and Lehman Go Cellular: CW Networks. Advances in Neural Information Processing Systems. 2021
4. <a id="bodnar2021topological"></a>Cristian Bodnar, Fabrizio Frasca, Yuguang Wang, Nina Otter, Guido F Montufar, Pietro Lio and Michael Bronstein. Weisfeiler and Lehman Go Topological: Message Passing Simplicial Networks. International Conference on Machine Learning. 2021
5. <a id="bunch2020simplicial"></a>Eric Bunch, Qian You, Glenn Fung and Vikas Singh. Simplicial 2-Complex Convolutional Neural Networks. TDA {&} Beyond. 2020
6. <a id="giusti2022cell"></a>Lorenzo Giusti, Claudio Battiloro, Lucia Testa, Paolo Di Lorenzo, Stefania Sardellitti and Sergio Barbarossa. Cell attention networks. arXiv preprint arXiv:2209.08179. 2022
7. <a id="giusti2022simplicial"></a>Lorenzo Giusti, Claudio Battiloro, Paolo Di Lorenzo, Stefania Sardellitti and Sergio Barbarossa. Simplicial Attention Networks. arXiv preprint arXiv:2203.07485. 2022
8. <a id="yang2023convolutional"></a>Maosheng Yang and Elvin Isufi. Convolutional Learning on Simplicial Complexes. arXiv preprint arXiv:2301.11163. 2023
9. <a id="yang2022simplicial"></a>Maosheng Yang, Elvin Isufi, Michael T Schaub and Geert Leus. Simplicial convolutional filters. IEEE Transactions on Signal Processing. 2022
10. <a id="schaub2021signal"></a>Michael T Schaub, Yu Zhu, Jean-Baptiste Seby, T Mitchell Roddenberry and Santiago Segarra. Signal processing on higher-order networks: LivinaEURtmon the edge... and beyond. Signal Processing. 2021
11. <a id="hajij2022simplicial"></a>Mustafa Hajij, Ghada Zamzmi, Theodore Papamarkou, Vasileios Maroulas and Xuanting Cai. Simplicial complex representation learning. Machine Learning on Graphs (MLoG) Workshop at 15th ACM International WSDM (2022) Conference, WSDM2022-MLoG ; Conference date: 21-02-2022 Through 25-02-2022. 2022
12. <a id="hajij2022high"></a>Mustafa Hajij, Karthikeyan Natesan Ramamurthy, Aldo Guzman-Saenz and Ghada Za. High Skip Networks: A Higher Order Generalization of Skip Connections. ICLR 2022 Workshop on Geometrical and Topological Representation Learning. 2022
13. <a id="hajij2020cell"></a>Mustafa Hajij, Kyle Istvan and Ghada Zamzmi. Cell Complex Neural Networks. NeurIPS 2020 Workshop TDA and Beyond. 2020
14. <a id="yang2022efficient"></a>Ruochen Yang, Frederic Sala and Paul Bogdan. Efficient Representation Learning for Higher-Order Data with Simplicial Complexes. Learning on Graphs Conference. 2022
15. <a id="lee2022sgatsg"></a>See Hian Lee, Feng Ji and Wee Peng Tay. SGAT: Simplicial Graph Attention Network. International Joint Conference on Artificial Intelligence. 2022
16. <a id="ebli2020simplicial"></a>Stefania Ebli, Michael Defferrard and Gard Spreemann. Simplicial Neural Networks. TDA {&} Beyond. 2020
17. <a id="roddenberry2022signal"></a>T Mitchell Roddenberry, Michael T Schaub and Mustafa Hajij. Signal processing on cell complexes. ICASSP 2022-2022 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP). 2022
18. <a id="roddenberryglaze2021principled"></a>T Mitchell Roddenberry, Nicholas Glaze and Santiago Segarra. Principled simplicial neural networks for trajectory prediction. International Conference on Machine Learning. 2021
19. <a id="chen2022bscnets"></a>Yuzhou Chen, Yulia R Gel and H Vincent Poor. BScNets: Block simplicial complex neural networks. Proceedings of the AAAI Conference on Artificial Intelligence. 2022
