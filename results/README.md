# Results

All numbers are from the paper. Best value per dataset and metric is in **bold**. CSV versions of every table are in this folder.

| File | Contents |
|---|---|
| [`table2_text_encoder_x_graph_encoder.csv`](table2_text_encoder_x_graph_encoder.csv) | Table II: text encoder × graph encoder |
| [`table3_baselines_all_cutoffs.csv`](table3_baselines_all_cutoffs.csv) | Table III: comparison with text-retrieval methods, all cutoffs |
| [`table4_cosine_similarity_ablation.csv`](table4_cosine_similarity_ablation.csv) | Table IV: cosine-similarity (no-graph) ablation |

## Table II. Text encoder × graph encoder

In-domain retrieval performance across processed YouCook-II and four WikiHow categories. MR-PMKG uses MiniLM + GAT on YouCook-II and MiniLM + R-GCN on the WikiHow categories.

**Processed YouCook-II**

| Embedding | GNN | NDCG@10 | Recall@10 | MRR |
|---|---|---|---|---|
| MiniLM | GAT | **0.7079** | **0.5189** | **0.9036** |
| MiniLM | RGCN | 0.6971 | 0.5114 | 0.8962 |
| MiniLM | HGT | 0.6892 | 0.5080 | 0.8855 |
| BGE-M3 | GAT | 0.6710 | 0.4925 | 0.8836 |
| BGE-M3 | RGCN | 0.6534 | 0.4597 | 0.8763 |
| BGE-M3 | HGT | 0.6211 | 0.4830 | 0.8558 |
| Qwen3 | GAT | 0.6763 | 0.4992 | 0.8470 |
| Qwen3 | RGCN | 0.6444 | 0.4767 | 0.8287 |
| Qwen3 | HGT | 0.5617 | 0.4207 | 0.7776 |

**WikiHow Food**

| Embedding | GNN | NDCG@10 | Recall@10 | MRR |
|---|---|---|---|---|
| MiniLM | GAT | 0.6806 | 0.5518 | 0.9058 |
| MiniLM | RGCN | **0.7221** | **0.5866** | **0.9282** |
| MiniLM | HGT | 0.6835 | 0.5492 | 0.9143 |
| BGE-M3 | GAT | 0.5943 | 0.4808 | 0.8369 |
| BGE-M3 | RGCN | 0.6144 | 0.4987 | 0.8457 |
| BGE-M3 | HGT | 0.5618 | 0.4514 | 0.8021 |
| Qwen3 | GAT | 0.5867 | 0.4776 | 0.8264 |
| Qwen3 | RGCN | 0.6034 | 0.4935 | 0.8332 |
| Qwen3 | HGT | 0.5368 | 0.4325 | 0.7876 |

**WikiHow Sports-Fitness**

| Embedding | GNN | NDCG@10 | Recall@10 | MRR |
|---|---|---|---|---|
| MiniLM | GAT | 0.7543 | 0.6940 | 0.9329 |
| MiniLM | RGCN | **0.7881** | **0.7241** | **0.9499** |
| MiniLM | HGT | 0.7182 | 0.6652 | 0.9004 |
| BGE-M3 | GAT | 0.6660 | 0.6141 | 0.8786 |
| BGE-M3 | RGCN | 0.6739 | 0.6247 | 0.8584 |
| BGE-M3 | HGT | 0.5888 | 0.5430 | 0.8021 |
| Qwen3 | GAT | 0.6490 | 0.6044 | 0.8574 |
| Qwen3 | RGCN | 0.6571 | 0.6132 | 0.8440 |
| Qwen3 | HGT | 0.5756 | 0.5426 | 0.7842 |

**WikiHow Computers**

| Embedding | GNN | NDCG@10 | Recall@10 | MRR |
|---|---|---|---|---|
| MiniLM | GAT | 0.8586 | 0.7712 | **0.9674** |
| MiniLM | RGCN | **0.8607** | **0.7756** | 0.9635 |
| MiniLM | HGT | 0.8157 | 0.7274 | 0.9563 |
| BGE-M3 | GAT | 0.7868 | 0.7024 | 0.9355 |
| BGE-M3 | RGCN | 0.7881 | 0.7113 | 0.9271 |
| BGE-M3 | HGT | 0.7128 | 0.6356 | 0.8929 |
| Qwen3 | GAT | 0.7786 | 0.6980 | 0.9295 |
| Qwen3 | RGCN | 0.7676 | 0.6879 | 0.9133 |
| Qwen3 | HGT | 0.6954 | 0.6257 | 0.8571 |

**WikiHow Health**

| Embedding | GNN | NDCG@10 | Recall@10 | MRR |
|---|---|---|---|---|
| MiniLM | GAT | 0.6913 | 0.5807 | 0.9166 |
| MiniLM | RGCN | **0.7339** | **0.6202** | **0.9352** |
| MiniLM | HGT | 0.6725 | 0.5647 | 0.8982 |
| BGE-M3 | GAT | 0.5841 | 0.4951 | 0.8246 |
| BGE-M3 | RGCN | 0.5962 | 0.5053 | 0.8281 |
| BGE-M3 | HGT | 0.5171 | 0.4327 | 0.7618 |
| Qwen3 | GAT | 0.5760 | 0.4875 | 0.8143 |
| Qwen3 | RGCN | 0.5874 | 0.4999 | 0.8080 |
| Qwen3 | HGT | 0.5157 | 0.4342 | 0.7541 |

## Table III. Comparison with text-retrieval methods (all cutoffs)

Comparison with established text-retrieval methods across processed YouCook-II and four WikiHow domains.

**Processed YouCook-II**

| Method | MRR | Recall@1 | Recall@5 | Recall@10 | NDCG@1 | NDCG@5 | NDCG@10 |
|---|---|---|---|---|---|---|---|
| BM25 | 0.5825 | 0.0387 | 0.1448 | 0.2308 | 0.4436 | 0.3560 | 0.3170 |
| SPLADE | 0.8038 | 0.0632 | 0.2548 | 0.4093 | 0.6998 | 0.6009 | 0.5481 |
| Contriever | 0.5780 | 0.0399 | 0.1657 | 0.2824 | 0.4386 | 0.3740 | 0.3554 |
| E5 | 0.6336 | 0.0484 | 0.1981 | 0.3142 | 0.5162 | 0.4471 | 0.4115 |
| ColBERTv2 | 0.8421 | 0.0666 | 0.2734 | 0.4311 | 0.7469 | 0.6483 | 0.5845 |
| IMRNNs | 0.8345 | **0.0975** | **0.3390** | 0.4727 | 0.7577 | 0.6311 | 0.5712 |
| E5-Mistral-7B | 0.2062 | 0.0112 | 0.0327 | 0.0451 | 0.1284 | 0.0849 | 0.0685 |
| GritLM-7B | 0.7990 | 0.0614 | 0.2485 | 0.3946 | 0.6824 | 0.5864 | 0.5319 |
| RepLLaMA-7B | 0.8301 | 0.0631 | 0.2661 | 0.4244 | 0.7189 | 0.6248 | 0.5684 |
| **MR-PMKG** | **0.9036** | 0.0743 | 0.3292 | **0.5189** | **0.8373** | **0.7731** | **0.7079** |

**WikiHow Food**

| Method | MRR | Recall@1 | Recall@5 | Recall@10 | NDCG@1 | NDCG@5 | NDCG@10 |
|---|---|---|---|---|---|---|---|
| BM25 | 0.7628 | 0.0677 | 0.2351 | 0.3505 | 0.6618 | 0.5139 | 0.4525 |
| SPLADE | 0.9458 | 0.0943 | 0.3537 | 0.5183 | 0.9099 | 0.7551 | 0.6663 |
| Contriever | 0.8920 | 0.0859 | 0.3118 | 0.4498 | 0.8290 | 0.6653 | 0.5790 |
| E5 | **0.9548** | **0.0960** | 0.3618 | 0.5255 | **0.9258** | 0.7724 | 0.6780 |
| ColBERTv2 | 0.9489 | 0.0948 | 0.3567 | 0.5240 | 0.9154 | 0.7616 | 0.6726 |
| IMRNNs | 0.8688 | 0.0838 | 0.3117 | 0.4532 | 0.7963 | 0.6575 | 0.5789 |
| E5-Mistral-7B | 0.5009 | 0.0374 | 0.1210 | 0.1840 | 0.3607 | 0.2657 | 0.2365 |
| GritLM-7B | 0.9390 | 0.0925 | 0.3395 | 0.4952 | 0.8974 | 0.7293 | 0.6391 |
| RepLLaMA-7B | 0.9526 | 0.0958 | 0.3616 | 0.5273 | 0.9226 | 0.7706 | 0.6783 |
| **MR-PMKG** | 0.9282 | 0.0929 | **0.3900** | **0.5866** | 0.8807 | **0.7938** | **0.7221** |

**WikiHow Sports-Fitness**

| Method | MRR | Recall@1 | Recall@5 | Recall@10 | NDCG@1 | NDCG@5 | NDCG@10 |
|---|---|---|---|---|---|---|---|
| BM25 | 0.7340 | 0.0978 | 0.2740 | 0.3674 | 0.6392 | 0.4633 | 0.4250 |
| SPLADE | 0.9088 | 0.1346 | 0.4238 | 0.5645 | 0.8592 | 0.6939 | 0.6404 |
| Contriever | 0.8644 | 0.1237 | 0.3812 | 0.5152 | 0.7946 | 0.6246 | 0.5808 |
| E5 | 0.9228 | 0.1371 | 0.4312 | 0.5756 | 0.8784 | 0.7079 | 0.6537 |
| ColBERTv2 | 0.8935 | 0.1305 | 0.4095 | 0.5589 | 0.8356 | 0.6734 | 0.6297 |
| IMRNNs | 0.8066 | 0.1157 | 0.3787 | 0.5106 | 0.7308 | 0.6063 | 0.5673 |
| E5-Mistral-7B | 0.6186 | 0.0746 | 0.2253 | 0.3131 | 0.4820 | 0.3674 | 0.3473 |
| GritLM-7B | 0.9102 | 0.1350 | 0.4113 | 0.5586 | 0.8550 | 0.6756 | 0.6293 |
| RepLLaMA-7B | 0.9251 | 0.1391 | 0.4257 | 0.5641 | 0.8845 | 0.7014 | 0.6448 |
| **MR-PMKG** | **0.9499** | **0.1572** | **0.5368** | **0.7241** | **0.9136** | **0.8287** | **0.7881** |

**WikiHow Computers**

| Method | MRR | Recall@1 | Recall@5 | Recall@10 | NDCG@1 | NDCG@5 | NDCG@10 |
|---|---|---|---|---|---|---|---|
| BM25 | 0.8297 | 0.1266 | 0.3555 | 0.4659 | 0.7625 | 0.5833 | 0.5409 |
| SPLADE | 0.9335 | 0.1507 | 0.4825 | 0.6422 | 0.9055 | 0.7688 | 0.7254 |
| Contriever | 0.9133 | 0.1393 | 0.4511 | 0.6149 | 0.8641 | 0.7295 | 0.6926 |
| E5 | 0.9596 | 0.1532 | 0.4989 | 0.6702 | **0.9378** | 0.8031 | 0.7577 |
| ColBERTv2 | 0.9367 | 0.1474 | 0.4784 | 0.6424 | 0.9018 | 0.7656 | 0.7249 |
| IMRNNs | 0.9426 | **0.1560** | 0.5264 | 0.6863 | 0.9097 | 0.8098 | 0.7696 |
| E5-Mistral-7B | 0.7134 | 0.0935 | 0.3018 | 0.4219 | 0.5987 | 0.4910 | 0.4684 |
| GritLM-7B | 0.9409 | 0.1494 | 0.4897 | 0.6585 | 0.9117 | 0.7796 | 0.7394 |
| RepLLaMA-7B | 0.9566 | 0.1527 | 0.5020 | 0.6707 | 0.9336 | 0.8045 | 0.7576 |
| **MR-PMKG** | **0.9635** | 0.1495 | **0.5621** | **0.7756** | 0.9358 | **0.8956** | **0.8607** |

**WikiHow Health**

| Method | MRR | Recall@1 | Recall@5 | Recall@10 | NDCG@1 | NDCG@5 | NDCG@10 |
|---|---|---|---|---|---|---|---|
| BM25 | 0.7697 | 0.0880 | 0.2602 | 0.3572 | 0.6854 | 0.5135 | 0.4515 |
| SPLADE | 0.9232 | 0.1132 | 0.3794 | 0.5337 | 0.8781 | 0.7195 | 0.6498 |
| Contriever | 0.8927 | 0.1063 | 0.3496 | 0.4868 | 0.8319 | 0.6705 | 0.5984 |
| E5 | 0.9311 | 0.1142 | 0.3828 | 0.5390 | 0.8897 | 0.7300 | 0.6581 |
| ColBERTv2 | 0.9213 | 0.1126 | 0.3799 | 0.5392 | 0.8762 | 0.7217 | 0.6548 |
| IMRNNs | 0.7623 | 0.0882 | 0.2941 | 0.4092 | 0.6643 | 0.5441 | 0.4936 |
| E5-Mistral-7B | 0.6063 | 0.0576 | 0.1824 | 0.2637 | 0.4668 | 0.3569 | 0.3214 |
| GritLM-7B | 0.9290 | 0.1135 | 0.3793 | 0.5302 | 0.8847 | 0.7221 | 0.6481 |
| RepLLaMA-7B | **0.9369** | 0.1152 | 0.3876 | 0.5453 | **0.8977** | 0.7396 | 0.6662 |
| **MR-PMKG** | 0.9352 | **0.1169** | **0.4311** | **0.6202** | 0.8920 | **0.7943** | **0.7339** |

### Additional results reported in the paper

- **LLaMA-2 70B on WikiHow Computers:** Recall@10 0.6702, NDCG@10 0.7571, MRR 0.9573 (not run on the other categories because of its computational cost).
- **YouCook-II benchmark query set (MR-PMKG):** Recall@1/5/10 = 0.9622 / 0.9989 / 0.9997; NDCG@1/5/10 = 0.9622 / 0.9840 / 0.9843.

## Table IV. Cosine-similarity (no-graph) ablation

See [`../appendix/README.md`](../appendix/README.md#c-cosine-similarity-no-graph-ablation).
