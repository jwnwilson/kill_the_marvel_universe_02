Kill the marvel universe Exercise

Please note the focus of this exercise is analyzing data and data science, I'm neglecting code quality to allow me to
focus on experimenting with new tools, this is not production friendly work flow.

Plan of attack:

- (DONE) Build simple scraper with grequests for character API use comic IDs as that's all we need save data into characters.json (check comic ID limit doesn't break anything)

- (DONE) Write a simple reporter to output all characters alphabetically

- (DONE) Write simple reporter to output top 10 heros by comics

- (DONE) Build a networkx graph using comic IDs to connect heros in graph

- (DONE) Use networkx to calculate centrality and get top 10

- (DONE) Render graph to show character connections

- (DONE) Calculate influence based on similar logic from previous project using nx.neighbors to get basic
  influence of character and the surrounding characters to n levels - Looks like similar results to
  degree algorithm already implemented so will need to investigate graph to make sure it's built
  correctly

- (DONE) After analysing the data, looks like the results could be correct but the amount of comic
  relations on each character is limited to 20 on initial API call I thought I checked this as per my
  notes, will have to go through characters for > 20 relations and make additional calls to get their extra relations

- (DONE) Added comic API scraping and after loading all the comic data got much more expected results

- Clean up project, remove redundant code, write tests and update coverage

- Reduce amount of comic data / character data stored from api scraper

- Highlight high influence characters on graph and remove low influence to make it easier to digest

- Use community to work out the communities in the marvel universe and then find the most connected community bridges that will cover the most communities (Might be very similar to betweeness centrality already calculated)

- Show reasons for going for community links based on research that they are the ones who need to be vaccinated first inepidemics to fight them. 

- Add instructions on how to run crawler and different algorithms on data


Usage:

Algorithm options:

- degree_centrality
- closeness_centrality
- eigenvector_centrality
- katz_centrality
- betweenness_centrality

$ marvel_reporter.py --algorithm $ALGORITHM -show_graph

e.g.

$ marvel_reporter.py --algorithm eigenvector_centrality
