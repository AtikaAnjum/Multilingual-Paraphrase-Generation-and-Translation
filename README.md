# Multilingual-Paraphrase-Generation--and-Translation

 The primary objective of this project is to design a system that can take an input sentence in one language, generate a paraphrased version in the same language, and then translate that paraphrased sentence into another target language such as French or German. This is an important step toward creating systems that can automatically produce high-quality multilingual content for applications such as localization, multilingual chatbots, and global customer-support systems.

To achieve this, I fine-tuned the pretrained facebook/mbart-large-50-many-to-many-mmt model using the GLUE MRPC dataset, which contains pairs of sentences that convey similar meanings. These pairs were used to teach the model how to generate paraphrases that preserve semantic equivalence while allowing for linguistic variation. The fine-tuning process incorporated LoRA (Low-Rank Adaptation), a parameter-efficient technique that modifies only specific parts of the model (such as query, key, and value projections) rather than all parameters. This approach significantly reduces computational cost and training time without compromising accuracy.

The project was implemented in Python using the Hugging Face Transformers, PEFT, and Datasets libraries within the Google Colab environment. During training, standard preprocessing techniques such as tokenization and padding were applied to prepare text for the model. The training parameters included a learning rate of 2e-5, batch size of 4, and three training epochs. Evaluation was performed using BLEU scores and sentence similarity metrics to measure how closely the paraphrased sentences matched their reference versions.

### for deeper understanding refer to the notebook .
