

What do I do with this ?
========================

Commandes à lancer une fois pour initialiser ElasticSearch :
docker build -t mappings:0.0.1 mappings
docker run -d -p 127.0.0.1:9411:9200 mappings:0.0.1

Commandes à ré-excécuter pour mettre à jour la donnée source et relancer le script de test des scénarios :  
docker build -t poseidon:0.0.1 .

docker run -ti --network=host -v /Users/leonardmaguin/onogone/code-du-travail-numerique-leo/code_travail_scenario/data:/data poseidon:0.0.1

docker run -ti --network=host -v ($PWD)/data:/data poseidon:0.0.1