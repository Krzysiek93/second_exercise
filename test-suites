def labels = ['A', 'B'] // labels for Jenkins nodes
def builders = [:]
for (x in labels) {
    def label = x 
    builders[label] = {
	node(label) {
		stage("X SUITE"){
			echo "CHECKOUT TESTS X"
			echo "RUN TESTS X"
		}
		stage("Y SUITE"){
			echo "CHECKOUT TESTS Y"
			echo "RUN TESTS Y"	
		}
		stage("CLENUP"){
			cleanWs()
		}
	 }
      }
}

parallel builders
