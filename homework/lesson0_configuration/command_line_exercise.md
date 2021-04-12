# Command Line Exercise Homework

FOR THE QUESTIONS 3-6,
PLEASE INCLUDE BOTH THE ANSWER AND THE COMMAND LINE COMMAND YOU USED TO GET THE ANSWER


#### 1. cd in to the configuration_files directory (raw_data/configuration_files )
DONE

#### 2. How many aws_config_files directories are there?
ls | wc -l

it is 5

#### 3. In which directory is config42.ini?
find . -name config42.ini

it is in aws_config_files_4

#### 4. Use a find, a pipe, and wc to count how many config files exist in aws_config_files_3
find aws_config_files_3 -name *.ini | wc -l

there are 19 files in that directory.

#### 5. What is the region specified in config33.ini
us-west-2

#### 6. Use grep to search which file contains the term 'exercise_answer'
grep -rwl . -e 'exercise_answer'

./raw_data/configuration_files/aws_config_files_4/config42.ini
42

#### 7.  Use $() to copy all of the .ini files into new directory called all_ini
mkdir all_ini
cp $(find . -name '*.ini') all_ini
