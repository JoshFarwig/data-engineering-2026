# homework 01

Q1-Q6: [Notebook answers](./docker-sql/docker-sql-homework.ipynb)

Q7: `terraform init, terraform apply -auto-approve, terraform destroy`

### useful gcloud commands

```bash
# login to gcloud cli: authenticate via browser
gcloud auth login

# login to adc (application default credentials):
# for local development with terraform and client libraries 
# (uses user account, no service account needed, also on the main.tf, using service account via terraform rather than through cli)
gcloud auth application-default login

# setup service account: create in iam console or via cli
gcloud iam service-accounts create [NAME]

# grant user access to impersonate service account
gcloud iam service-accounts add-iam-policy-binding SA_EMAIL --member="user:USER_EMAIL" --role="roles/iam.serviceAccountTokenCreator"

# use service account key file: 
# for ci/cd or when you need to use a specific service account (not needed for local terraform if using adc)
export GOOGLE_APPLICATION_CREDENTIALS=/path/to/key.json
```
