# scarlett_G1_conf
Script for dumping and loading configuration of scarlett 18i20 audio interface
It is a modification of https://github.com/tseaver/scarlett_yaml. In the initial scarlett_yaml script, there were parameters with more argument than expect creating the following error on a scarlett 18i20 audio interface:
line 403, in _extract_controls
    num_id, _, name = line.split(b",")
ValueError: too many values to unpack (expected 3)

I have only modify the dump version yet with the correct parametezrs. DONT USED YOUR DUMPED FILE TO LOAD INTO The interface (not the same structure)
Use a file given as examples:
scarlett-18i20-default.yaml

To dump the parameters to the standard output: python3 scarlett_yaml.py
To dump the parameters to a file : python3 scarlett_yaml.py > file.yaml
to load a parameter from a file: python3 scarlett_yaml.py load file.yaml

In my case, the output where mutted at poweron. I load the file scarlett-18i20-default.yaml to the interface after poweron.
yaml files are easy to modify by a human.
