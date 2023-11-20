## SageMaker Pipelines Notebook Job Step Example

In this example we explore using Notebook Job steps to orchestrate ML workflows within SageMaker Pipelines. In this example we specifically build a Pipeline that solves an NLP Text Classification use-case. We use the public SST2 dataset with a BERT Transformers model for Binary Text Classification on sample labels. The notebooks within the repository are listed below to give further clarity on how the example is structured. 

- <b>nb-job-pipeline.ipynb</b>: This is the main orchestration notebook, here we execute the different notebooks as Notebook Job Steps and stitch them together into a singular SageMaker Pipeline.
- <b>preprocess.ipynb</b>: Notebook that pulls down the SST2 dataset and structures it into a format the BERT model can understand.
- <b>training.ipynb</b>: Takes the dataset from the previous Notebook Job Step and runs local training within the notebook.
  - <b>prepare-test-set.ipynb</b>: Is a notebook that training notebook is dependent on. The notebook prepares a test dataset, that the trained model runs Batch Inference on.
- <b>transform-monitor.ipynb</b>: Takes the pre-trained BERT model and runs Batch Inference and also sets up Data Quality Model Monitoring with a Baseline Dataset.

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

