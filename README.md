## Introduction

Welcome! This is the Novel Aficionados dataset. It was created for the experiments carried out in Bruera and Herbelot (Forthcoming). If you have any question, you can contact Andrea Bruera at a.bruera@qmul.ac.uk. 

This dataset contains a collection of 59 out-of-copyright novels, that we obtained from Project Gutenberg (http://www.gutenberg.org/), an online library of free eBooks. 

## Why this dataset?

This dataset was created for a specific, original NLP task, the Doppelgänger test, which focuses on evaluating the distributional representations of individual entities (the characters present in the novels). The Doppelgänger test evaluates whether each entity representation learned in one subcorpus (one half of a novel) can be correctly matched to its co-referring entity representation from another subcorpus (the second half of the same novel), choosing among all the other entity representations. The task is challenging in that the model must distinguish between very similar entities (people and entities engaged in shared activities in a common universe) using scarce data.

## Main features

The main features of this dataset are the following:

- Only novels having a Wikipedia entry were selected, in order to carry out a cross-document referential task (see the paper);
- Novels are present in both their original gutenberg.org version and in their pre-processed versions (see notes below in the folder structure);
- Novels were analyzed with the BookNLP toolkit (https://github.com/dbamman/book-nlp) and the resulting files, which were used in our original paper, are also included, so you don't have to run the BookNLP pipeline again.
- For each novel, this dataset contains also the text of their Wikipedia page (entries were downloaded at the time of our work, around late 2019).

## Folder structure

Here is an example of a folder structure, together with short descriptions of the contents:

├── A\_Christmas\_Carol\_by\_Charles\_Dickens\_                       *(Each novel comes with its own folder)*  
│   ├── original\_files                        *(This folder contains the original files from gutenberg.org, Wikipedia and BookNLP)*  
│   │   ├── book\_nlp\_output  
│   │   │   ├── 19337.tokens  
│   │   │   ├── book.id.book  
│   │   │   └── book.id.html  
│   │   ├── original\_novel  
│   │   │   └── 19337.txt  
│   │   └── original\_wikipedia\_page  
│   │       └── 19337.txt  
│   └── test\_files                        *(This folder contains the pre-processed files used in our experiments)*  
│       ├── characters\_list\_19337.txt                        *(The list of the characters, together with all their aliases and frequencies)*  
│       ├── matched\_common\_nouns\_list\_19337.txt                        *(The list of common nouns used in our experiments, matched for frequency to the proper names)*  
│       ├── novel                        *(Various versions of the pre-processed novel)*  
│       │   ├── 19337\_no\_header.txt                        *(Version with little-to-no preprocessing, where only the gutenberg.org header is cut out)*  
│       │   ├── matched\_19337\_ready\_for\_any\_testing.txt                        *(Pre-processed version, divided in paragraphs, with no special symbols, using the common nouns of matched\_common\_nouns\_list\_19337.txt)*  
│       │   ├── matched\_19337\_ready\_for\_replication.txt                        *(Like above, but with symbols indicating differently proper names and common nouns - e.g. $sherlock_holmes$ and #book#)*  
│       │   ├── unmatched\_19337\_ready\_for\_any\_testing.txt                        *(Pre-processed version, divided in paragraph, using the most frequent common nouns of unmatched_common_nouns_list_19337.txt)*  
│       │   └── unmatched\_19337\_ready\_for\_replication.txt  
│       ├── unmatched\_common\_nouns\_list\_19337.txt                        *(The list of common nouns used in another setup for our experiments, NOT matched for frequency to the proper names)*  
│       └── wikipedia\_page                        *(This folder contains the Wikipedia pages, with the same internal organization as the folder above)*  
│           ├── 19337\_no\_header.txt  
│           ├── matched\_19337\_ready\_for\_any\_testing.txt  
│           ├── matched\_19337\_ready\_for\_replication.txt  
│           ├── unmatched\_19337\_ready\_for\_any\_testing.txt  
│           └── unmatched\_19337\_ready\_for\_replication.txt  

## The novels

The list of the folders (and of the novels) is as follows:

* A_Christmas_Carol_by_Charles_Dickens_
* A_Christmas_Carol_in_Prose_Being_a_Ghos
* A_Study_in_Scarlet_by_Arthur_Conan_Doyle
* A_Tale_of_Two_Cities_by_Charles_Dickens_
* Adventures_of_Huckleberry_Finn_by_Mark_T
* Alices_Adventures_in_Wonderland_by_Lewi
* Anna_Karenina_by_graf_Leo_Tolstoy_
* Anne_of_Green_Gables_by_L_M__Montgomer
* Anthem_by_Ayn_Rand_
* Beowulf_An_AngloSaxon_Epic_Poem_
* Candide_by_Voltaire_
* Don_Quixote_by_Miguel_de_Cervantes_Saave
* Dracula_by_Bram_Stoker_
* Dubliners_by_James_Joyce_
* Emma_by_Jane_Austen_
* Et_dukkehjem_English_by_Henrik_Ibsen_
* Ethan_Frome_by_Edith_Wharton_
* Frankenstein_Or_The_Modern_Prometheus_
* Great_Expectations_by_Charles_Dickens_
* Hard_Times_by_Charles_Dickens_
* Jane_Eyre_An_Autobiography_by_Charlotte
* Le_Morte_dArthur_Volume__by_Sir_Thoma
* Les_Misérables_by_Victor_Hugo_
* Little_Women_by_Louisa_May_Alcott_
* Metamorphosis_by_Franz_Kafka_
* Moby_Dick_Or_The_Whale_by_Herman_Melvi
* Narrative_of_the_Life_of_Frederick_Dougl
* Oliver_Twist_by_Charles_Dickens_
* Persuasion_by_Jane_Austen_
* Peter_Pan_by_J_M__Barrie_
* Prestuplenie_i_nakazanie_English_by_Fyo
* Pride_and_Prejudice_by_Jane_Austen_
* Pygmalion_by_Bernard_Shaw_
* Sense_and_Sensibility_by_Jane_Austen_
* Siddhartha_by_Hermann_Hesse_
* The_Adventures_of_Tom_Sawyer_by_Mark_Twa
* The_Brothers_Karamazov_by_Fyodor_Dostoye
* The_Count_of_Monte_Cristo_Illustrated_b
* The_Hound_of_the_Baskervilles_by_Arthur_
* The_Iliad_by_Homer_
* The_Importance_of_Being_Earnest_A_Trivi
* The_Jungle_by_Upton_Sinclair_
* The_Legend_of_Sleepy_Hollow_by_Washingto
* The_Mysterious_Affair_at_Styles_by_Agath
* The_Picture_of_Dorian_Gray_by_Oscar_Wild
* The_Scarlet_Letter_by_Nathaniel_Hawthorn
* The_Secret_Garden_by_Frances_Hodgson_Bur
* The_Sign_of_the_Four_by_Arthur_Conan_Doy
* The_Strange_Case_of_Dr_Jekyll_and_Mr_H
* The_Time_Machine_by_H_G__Wells_
* The_Tragical_History_of_Doctor_Faustus_b
* The_Turn_of_the_Screw_by_Henry_James_
* The_War_of_the_Worlds_by_H_G__Wells_
* The_Wonderful_Wizard_of_Oz_by_L_Frank__
* The_Yellow_Wallpaper_by_Charlotte_Perkin
* Treasure_Island_by_Robert_Louis_Stevenso
* Uncle_Toms_Cabin_by_Harriet_Beecher_Sto
* War_and_Peace_by_graf_Leo_Tolstoy_
* Wuthering_Heights_by_Emily_Brontë_
