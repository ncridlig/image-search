# image-search
Goal: Solve a **metric learning** problem. Open world retrieval of objects with 1 or more training examples.
## Research

https://medium.com/data-science/building-an-image-similarity-search-engine-with-faiss-and-clip-2211126d08fa

https://www.trychroma.com

https://milvus.io/it

https://openai.com/index/clip/

## Preprocessing
- CLIP is already invariant to all lighting transformations
- CLIP captures meaning from the entire photo, therefore there is a requirement to preprocess to find painting
  - Option 1: Use a [Hough Transform](https://github.com/luczeng/HoughRectangle) to detect rectangles
  - Option 2: Use a [neural network](https://huggingface.co/docs/transformers/en/tasks/semantic_segmentation) to segment painting
  - Option 3: Use an off the shelve [Product Recogntion Service](https://cloud.google.com/vision-ai/docs/product-recognizer) to detect key items
