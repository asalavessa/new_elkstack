IMPORTANT: 

"ERROR: [1] bootstrap checks failed. You must address the points described in the following [1] lines before starting Elasticsearch.
bootstrap check failure [1] of [1]: max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]"

    If your elastic search containers keep crashing with the above error message, run the following command before the "docker-compose up":
     --> "sudo sysctl -w vm.max_map_count=262144";
    
    
1) GENERATE CERTIFICATES:
        "docker-compose -f create-certs.yml run --rm create_certs"
        
2) RUN THE CONTAINERS:
        "docker-compose up"
