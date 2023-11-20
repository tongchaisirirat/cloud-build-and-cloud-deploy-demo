# cloud-build-and-cloud-deploy-demo

# 0.IAM
autopilot not set iam



# 1.Create 2 GKE clusters
gcloud container --project "devops-sandbox-2023" clusters create-auto "autopilot-cluster-mind-test" --region "asia-southeast1" --release-channel "regular" --network "projects/devops-sandbox-2023/global/networks/default" --subnetwork "projects/devops-sandbox-2023/regions/asia-southeast1/subnetworks/default" --cluster-ipv4-cidr "/17"

gcloud container --project "devops-sandbox-2023" clusters create-auto "autopilot-cluster-mind-prod" --region "asia-southeast1" --release-channel "regular" --network "projects/devops-sandbox-2023/global/networks/default" --subnetwork "projects/devops-sandbox-2023/regions/asia-southeast1/subnetworks/default" --cluster-ipv4-cidr "/17"

# 2.Create cloud build

 create 



# Step 3: Preparing our configuration:

.
├── index.html
├── Dockerfile
├── skaffold.yaml
├── deployment.yaml
├── cloudbuild.yaml
├── clouddeploy.yaml
└──README

export PROJECT_ID=devops-sandbox-2023
gcloud deploy apply --file clouddeploy.yaml --region=asia-southeast1 --project=devops-sandbox-2023

# Step 4

git add .
git commit -m “Added Version 1 in index.html”
git push --all origin
 or 

 git add . && git commit -m “test” && git push --all origin
# Step 5

