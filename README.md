# KBLI and KBJI predictor

This Python script create KBLI and KBJI prediction based on the job description from Excel or CSV file. Designed to help in evaluating collected Surveys data.

## Features

- Preprocess input file (stemming, removing stopwords, vectorizing and tokenize).
- Create KBLI and KBJI prediction based on input.
- Create a comparison between prediction result and the current input.
- Outputs results to a single Excel file acting as comparison.

## Academic Papers

*Waiting for release

## Prerequisites

- Python 3.6 or higher
- pandas
- openpyxl
- nltk
- PySastrawi
- Scikit-learn 1.4.1.post1

## Installation

1. Clone this repository.
2. Install the required packages:

```bash
pip install pandas openpyxl nltk pysastrawi scikit-learn==1.4.1.post1
```

## Usage

1. Open svm_predict.ipynb in your favorite notebook environment

2. Change the INPUT into the path of your query result and OUTPUT into the path where you want to save the result:

   ```
   INPUT = 'sqllab_untitled_query_1_20240821T043054.csv'
   OUTPUT = 'hasil_pemeriksaan_KBLI_KBJI_2024-8-21.xlsx' 
   ```

3. Run the script.

4. The script will create a prediction based on the description and made comparison with the input code.

## Input Data Structure

| usaha  | produk | bidang | kbli | kbli_label | kbji | kbji_label|
| --- | --- | --- | --- | --- | --- | --- |
| ... | ... | ... | ... | ... | ... | ... |

Otherwise, use the result from the following [Query](https://fasih-dashboard.bps.go.id/superset/sqllab/?savedQueryId=8701) (need VPN).

## Performance

| Evaluation | SVC_KBLI | SVC_KBJI |
| --- | --- | --- |
| Precision | 0,72646194970342 | 0,6200531051097260 |
| Recall | 0,7368978295394380 | 0,6357162421254450 |
| F1 | 0.7207170411743122 | 0.6188023969509172 |

## Notes

- The model used was trained using West Nusa Tenggara August 2023 Socioeconomic Survey data.
- Currently, the model can only predict 272 KBLI (details in KBLI.csv) and 164 KBJI (details in KBJI.csv) code .
- Because of training data limitation on the current stage, please use only for comparison purpose only.

## Contributing

Feel free to fork this repository and submit pull requests with any improvements or bug fixes.

## Author

- **Terry Devara Tri Saadi**
- Email: <devatrisa@gmail.com>
- **Agnes Septi Dwicahayaniawan**
- Email: <agnes.cahaya0409@gmail.com>

## License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT).
