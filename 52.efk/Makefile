elasticsearch:
	helm repo add elastic https://helm.elastic.co
	helm install elasticsearch  elastic/elasticsearch --namespace efk --create-namespace --set replicas=1 --set minimumMasterNodes=1

kibana:
	helm install kibana  elastic/kibana


expose:
	kubectl port-forward 
