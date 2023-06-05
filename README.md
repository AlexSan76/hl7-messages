# hl7-messages
hl7-messages


Check examples here

[Examples](https://docs.google.com/document/d/1CAQriFgmUk91mwzCPn8rjKWjirG0vSsq9kB90zbpKCc/edit#)



https://drive.google.com/drive/folders/19KPgujbTT81b48Hee1p9ieDfFWPIo-ur




https://code.roche.com/lni/modules/system-test/-/blob/master/data/hl7/OrderCreated.hl7

https://code.roche.com/ppa/messages/message_repository/-/tree/main/new_order/messages

PPX Messages
https://docs.google.com/document/d/1Mu5gi07ijWHQXy7AASrVJWu2pwjsAHh2coq1lWq13zg/edit#


PPX XML
https://code.roche.com/connectivity/cslite/-/tree/nci_ppx/

Port forwarding to cobas-pro


´´´

export KUBECONFIG='/Users/sandina/.kube/nci-edge-dev.yaml'
kubectl port-forward svc/cslite-passthrough-mock-lab-cobaspro-1-inbound -n team-lni-environment 55662:55662
´´´
 

 send by command hl7


 echo -n -e "\x0b$(cat hl7v2-mllp-ack-sample.txt)\x1c\x0d" | nc -q1 -lv -p 2525 | less


 echo -n -e "\x0b$(cat hl7v2-mllp-ack-sample.txt)\x1c\x0d" | nc -lv -p 55662 | less



port foorward kodama dev 2

export KUBECONFIG='/Users/sandina/.kube/ni-kodama2-dev.yaml'
kubectl port-forward svc/host-adapter -n team-lni-environment 55662:55662
ni-ppx-preintegration.yaml
export KUBECONFIG='/Users/sandina/.kube/ni-kodama3-dev.yaml'
kubectl -v=8 port-forward svc/host-adapter-nst -n team-lni-environment 55662:55662
kubectl port-forward svc/host-adapter-nst -n team-lni-environment 55662:55662

export KUBECONFIG='/Users/sandina/.kube/ni-kodama3-dev.yaml'

Cobaspro
export KUBECONFIG='/Users/sandina/.kube/ni-kodama2-dev.yaml'
kubectl port-forward svc/host-adapter-nst -n team-lni-environment 55662:55662

nst

[15:45:55] Connected to 127.0.0.1:55662
[15:45:55] Message sent 
[15:45:55] ACK Received: 
MSH|^~\&|nst|orm|lis_cbt|cbt|20221114143331||ORL^O34^ORL_O34|97e7801b-e798-4469-a5bf-0d8ba4dee359|P|2.5.1||||||UNICODE UTF-8|||
MSA|AA|8f283199-8c43-446e-a92f-4ac465079a7b

[15:45:55] Connection to 127.0.0.1:55662 has been closed 




export KUBECONFIG='/Users/sandina/.kube/ni-ppx-preintegration.yaml'
kubectl port-forward svc/instrument-adapter -n team-lni-environment 55662:55662