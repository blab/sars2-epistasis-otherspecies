# About

This repository analyzes the evolution SARS-CoV-2 after host jumps from human to other species. 
It builds a phylogeny enriched in SARS-CoV-2 genomes sampled from those other species, and places these sequences in context
of viral genomes samples from humans in order to infer host jump events and analyze the subsequent evolution that occurs. 
The phylogeny is built using [Nextstrain](https://nextstrain.org) to understand how SARS-CoV-2, the virus that is responsible for the COVID-19 pandemic, evolves and spreads. 
This workflow is copied from [github.com/nextstrain/ncov](https://github.com/nextstrain/ncov).

# Running


Use the following commons to run a build enriched for genomes sequenced from 
-mink:
```
nextstrain build --aws-batch --cpus 16 --memory 64GiB --detach . --set-threads tree=16 --profile species_profiles --configfile species_profiles/mink_builds.yaml
```

-deer:
```
nextstrain build --aws-batch --cpus 16 --memory 64GiB --detach . --set-threads tree=16 --profile species_profiles --configfile species_profiles/deer_builds.yaml
```

-cats:
```
nextstrain build --aws-batch --cpus 16 --memory 64GiB --detach . --set-threads tree=16 --profile species_profiles --configfile species_profiles/cat_builds.yaml
```

-dogs:
```
nextstrain build --aws-batch --cpus 16 --memory 64GiB --detach . --set-threads tree=16 --profile species_profiles --configfile species_profiles/dog_builds.yaml
```
