# de-duplications

Notebook for removing potential duplicates from EMLO. This script creates two files: one with letters removed either because they are duplicates or because they have been marked for deletion for one of a number of reasons. The second file includes the above but also removes all letters where either the sender or recipient is unknown. 

Steps:

1: Load 'EMLO_Matched_Works_2020.6.4.xlsx' and keep one of each 'cluster' of matched letters.  

2: Make a list of letters which 1) are part of a group of more than one sent on the same day between the same two people and 2) are NOT in the same catalogue. Keep only one of each of these groups.  

3: Remove all letters from test catalogues: 'Test_Pennant (test)', 'TESTS_Bayle', 'Test_Metadata test', 'TEST_Newton', 'Coornhert, Dirck Volckertszoon (test)' 

4: Load 'EMLO_LettersMarkedToDelete_2021.5.24.xlsx' and remove these letters  

5: Create a file called 'to_remove.csv' with a list of all letter IDs to remove. Has a header row called 'value'. Archive an old version of the file if any changes are detected.  

6: Remove any letters where either sender or recipient ID are one of: '903934','23155', '6854', '853', '923980', '270', '300827', '901925', '906141'. Create a file called ''to_remove_list_with_unknown.csv' with all of these letters plus the above.  

Both the to_remove_list and the to_remove_list_with_unknown have a 'reason' field with either:

* auto_duplication: letter was removed because it was identified as a duplication using the method desrcibed in step 2 above.
* from_emlo_matches: letter removed because of appearance in EMLO_Matched_Works_2020.6.4.xlsx
* test_catalogue: from a test catalogue which has not been published/finished
* marked_to_delete: appearance in EMLO_LettersMarkedToDelete_2021.5.24.xlsx
* author_or_recipient_unknown: either author or recipient found in the list of IDs in step 6 above.
