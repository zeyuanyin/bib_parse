# DBLP .bib File Format

Online search and format .bib file from DBLP.

The running speed depends on the network speed of accessing DBLP.

## Environments

```
pip install -r requirements.txt
```

After installing the requirements, you should download the NLTK data by running the following script:

```
import nltk
nltk.download('punkt')
nltk.download('averaged_perceptron_tagger')
```
## Usage

### Single Query via DBLP API

```
python dblp_request.py --query "Densely Connected Convolutional Networks"
```

### .bib File Format

```
python format_bib.py --input_file "input.bib" --output_file "output.bib"
```

python format_bib.py --input_file "input_short.bib" --output_file "output_short.bib"


python format_bib.py --input_file "input.bib" --output_file "output.bib"


python format_bib.py --input_file "input_ok.bib" --output_file "output_ok.bib"


- A journal's .bib contains 7 info: "author", "title", "journal", "volume", "number", "pages", "year" (if any).
- A conference's .bib contains 5 info: "author", "title ", "booktitle", "pages", "year" (if any).
- `no abbr` and `not found` bibtex is placed at the end of the output file and **need to be checked manually**.
- More than one bibtex will all be saved, may cause duplicate bibtex (`Repeated entry` error in latex).