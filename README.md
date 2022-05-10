Overview
=========
The test_graph web service handles HTTP requests to find the shortest path between 2 nodes based on the weighted network
loaded from JSOM file. It supports in direct/undirect/multi-direct and multi-undirect graphs. 

Algorithm
==========
The graph's functionality is defined in GraphFunctions classes which its relevant functionalities are called from the
accordance API in main.
Upon starting, the web service loads the network nodes and edges and create the relevant graph.
On short_path HTTP request, it returns the shortest path based on the weight of the edges. It uses the
Dijkstra’s Method to compute the shortest weighted path between two nodes in a graph.

On update_weight HTTP request, it checks that there is an edge between the 2 nodes and updates its weight. 

How to Run
===========
1. Download the compressed file.
2. Uncompress it on /tmp (tar -xzvf <tar_file>)
   1. The graph file, test-graph.json, is located under /tmp/via/docker/conf/
3. Change directory to /tmp/via/docker/
4. Run the command 'docker-compose up test_graph'
5. The web service is listening on http://127.0.0.1:8000
