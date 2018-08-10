# DialogWAE

It is a PyTorch implementation of the DialogWAE model described in
**DialogWAE: Multimodal Response Generation with Conditional Wasserstein Auto-Encoder**.
See the [paper](https://arxiv.org/abs/1805.12352) for more details. 

# Prerequisites
 - PyTorch 0.4.0
 - Python 3.6
 - Numpy
 - NLTK
 - You may need to pip install beeprint if the module is missing

# Usage
## Train
- Use pre-trained Word2vec
Download Glove word embeddings from https://nlp.stanford.edu/projects/glove/
The default setting use 200 dimension word embedding trained on Twitter.

At last, set **word2vec_path** at line 15 of train.py.

- Modify the arguments at the top of train.py as follows:

- Train model by
    ```python train.py```
The logs and temporary results will be printed to stdout and saved in the `./output` path.

## Test
Modify the arguments at the bottom of sample.py
    
Run model testing by:

    python sample.py
The outputs will be printed to stdout and generated responses will be saved at `results.txt` in the `./output` path.


# References 
If you use any source code included in this toolkit in your work, please cite the following paper. The bibtex are listed below:
 
    [Gu et al, 2018]:
     @article{gu2018dialogwae,
      title={Dialog{WAE}: Multimodal Response Generation with Conditional Wasserstein Auto-Encoder},
      author={Gu, Xiaodong and Cho, Kyunghyun and Ha, Jung-Woo and Kim, Sunghun},
      journal={arXiv preprint arXiv:1805.12352},
      year={2018}
    }

# LICENSE

Copyright 2018 NAVER Corp.
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright
   notice, this list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright
   notice, this list of conditions and the following disclaimer in the
   documentation and/or other materials provided with the distribution.

3. Neither the names of Facebook, Deepmind Technologies, NYU, NEC Laboratories America
   and IDIAP Research Institute nor the names of its contributors may be
   used to endorse or promote products derived from this software without
   specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF
SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS
INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN
CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
POSSIBILITY OF SUCH DAMAGE.