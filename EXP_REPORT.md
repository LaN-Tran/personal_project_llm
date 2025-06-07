# Experiment report

## in `vietnamese_embed_databse.ipynb`

- 1. Comparison between `Mistral-Nemo-Instruct-2407-Q4_K_M.gguf` and `vinai/phobert-base`

| Parameter                  |                                          |                     |
|--------                    | --------                                 | -------             |
| model                      | `Mistral-Nemo-Instruct-2407-Q4_K_M.gguf` | `vinai/phobert-base`|
| emebedding size            | 5120                                  | 768                |
| speed                      | 169 samples, each with ~200 words / 222 min                                 | 1080 samples each with ~ 100 word / < 60 min                 |
| cosine based on emebedding | quite good                                    | better?                | 

## in `Local_GenAi_code.ipynb`

- 1. experimenting with gguf llm supporting Vietnamese

  - 1.1 `TheBloke/Llama-2-7B-vietnamese-20k-GGUF` - `llama-2-7b-vietnamese-20k.Q4_K_M.gguf`: BAD.
  The model can not even reply to a simple English question.
  The model even produce meaningless reply to vietnamese input.
  There is probably error when transforming `Llama-2-7B-vietnamese` into `gguf` model?

  - 1.2 `tensorblock/bloomz-3b-GGUF` - `bloomz-3b-Q4_K_M.gguf`: compared to 1.1, much better

  - 1.3 `bartowski/Mistral-Nemo-Instruct-2407-GGUF` - `Mistral-Nemo-Instruct-2407-Q4_K_M.gguf`: compared to 1.2, its reponses are even much better, but it takes 45 min to answer.? whether the time it takes to reply compared to the context length? or depends on the complexity of the question (because model spends lots of time on the evaluation)? 

  - 1.4 using the local `bartowski/Mistral-Nemo-Instruct-2407-GGUF` - `Mistral-Nemo-Instruct-2407-Q4_K_M.gguf` to generate embeddings takes a lot of computation (in a computer with 4 logical cpu cores, all works 100%, it takes 238 min to embed 167 200-word paragraphs)

  - 1.5 using api call to "open-mistral-nemo" for generating embeddings: FAILURE. The call only to generate text.

  - 1.6 using another small model (BERT like) for generating embeddings, for example:

    - 1.6.1 [dangvantuan/vietnamese-embedding](https://huggingface.co/dangvantuan/vietnamese-embedding)
 
    - 1.6.2 [vinai/phobert-base](https://huggingface.co/vinai/phobert-base)

  - 1.7 Try out [vinai/PhoGPT-4B-Chat-gguf](https://huggingface.co/vinai/PhoGPT-4B-Chat-gguf)
- 2. experimenting with Mistral ai API

 - according to [Mistral AI model list](https://docs.mistral.ai/getting-started/models/models_overview/), the best open model `Mistral Nemo` - `open-mistral-nemo` is for multilanguage, including Vietnamese. The API call to the model gives very good response, and very fast. But if the document is confidential, it is not recommended. 

## Folder `data/`

- [1] [Phap Luat Viet Nam](https://thuvienphapluat.vn/van-ban/Tien-te-Ngan-hang/Nghi-quyet-148-NQ-CP-2023-tiep-tuc-trien-khai-thi-hanh-Nghi-quyet-42-2017-QH14-579993.aspx?v=tvpl-hdsd-firsr&step=step7)

  - the account: email: lanspaming06@gmail.com / username: Tr_Le_Ph_La/ pass: PhapLuanVN/ phone: 0962047087

  