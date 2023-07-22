# GSP1022
## Run in cloudshell
### It will ask enter a value type `yes`
### After yes wait few minutes and it will ask y or n type `n` and it will again ask type `n`
```cmd
git clone https://github.com/wwce/gcp-vmseries-tf-ilbnh-tags
cd gcp-vmseries-tf-ilbnh-tags
terraform init
terraform apply
gcloud compute instances remove-tags us-east1-vm --tags=$(gcloud compute instances describe us-east1-vm --zone=us-east1-b --format="value(tags.items.join(','))")
gcloud compute instances add-tags us-east1-vm --tags=us-east1-fw,us-west1-fw
```
