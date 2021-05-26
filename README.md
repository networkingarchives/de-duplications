# de-duplications
Notebook for removing potential duplicates from EMLO

Steps:

1: Load 'EMLO_Matched_Works_2020.6.4.xlsx' and keep one of each 'cluster' of matched letters.
2: Make a list of letters which 1) are part of a group of more than one sent on the same day between the same two people and 2) are NOT in the same catalogue. Keep only one of each of these groups.
3: Remove all letters from test catalogues: 'Test_Pennant (test)', 'TESTS_Bayle', 'Test_Metadata test', 'TEST_Newton', 'Coornhert, Dirck Volckertszoon (test)'
4: Load 'EMLO_LettersMarkedToDelete_2021.5.24.xlsx' and remove these letters
5: Create a file called 'to_remove.csv' with a list of all letter IDs to remove. Has a header row called 'value'. Archive an old version of the file if any changes are detected.
6: Remove any letters where either sender or recipient ID are one of: '903934','23155', '6854', '853', '923980', '270', '300827', '901925', '906141'. Create a file called ''to_remove_list_with_unknown.csv' with all of these letters plus the above.

