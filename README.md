# Recommending-code-tokens-via-N-gram-models
> This project is solely based on the assignment given by the instructor for the course Artificial Intelligence for Software Engineering (CSCI-680-01).


# Table of Contents  

- [Prerequisites](#prerequisites)
- [Data Collection](#data-collection)
- [Data Pre-processing](#data-pre-processing)
- [N-gram model](#n-gram-model)
- [How to run](#how-to-run)


## Prerequisites
* Python
  > `python version >=3.10.x`
* To save file in the docx format
  > `pip install python-docx`

* To send the request to the server
  > `pip install requests`
* Nataral Language Toolkit
   > `pip install nltk`





## Data Collection
> For every project data collection is a very important part. Researchers spent most of the time to collect the data also pre-process data. In order to collect the data, I used [SEART](https://seart-ghs.si.usi.ch/) website. By using this website anyone can collect any amount of github repositories. For this project, I only choose those repo which has at least **5000** commit. <br>
> After collecting the repositories, I've saved it in a csv file. After that I used **Python Script** to extract only java code from the repositories and saved all the files into docx file.<br>



Example of how I got data from the csv file and saved it to the word file.
~~~python
df = pd.read_csv('results.csv')
for i in range(1, 1001):
    try:
        repo_owner, repo_name = df.at[i, 'name'].split('/')
        java_files = extract_java_files_from_github(repo_owner, repo_name)

        if java_files:
            save_to_word(doc, java_files, repo_owner, repo_name)
    except Exception as e:
        print(f'Error processing {df.at[i, "name"]}: {e}')
~~~

## Data Pre-processing
>Data preprocessing is the process of transforming raw data into a format that's easier to analyze and understand. It's a fundamental step in any projects, and is often performed before data analysis or machine learning modeling.


## N-gram model
>A word n-gram language model is a purely statistical model of language. It has been superseded by recurrent neural network–based models, which have been superseded by large language models

## How to run
* Clone the repository
  > `git clone https://github.com/robiul-islam-rubel/Recommending-code-tokens-via-N-gram-models`
* Change directory
   > `cd Recommending-code-tokens-via-N-gram-models`









