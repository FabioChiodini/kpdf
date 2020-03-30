# kpdf
Lambda to transform json in PDF

Deploy using serverless https://serverless.com/

# Deploment notes

launch the commands from a cloud9 instance

clean all cloudofmration errors and delete bucket kiodo-vault-pdf

install serverless

curl -o- -L https://slss.io/install | bash

git clone https://github.com/FabioChiodini/kpdf.git

cd kpdf

sls plugin install -n serverless-python-requirements

sls deploy

docker image prune -a

test with 

curl -d '{"filename":"my-sample-filename.pdf", "html":"<html><head></head><body><h1>Custom HTML -> Posted From CURL as {JSON}</h1></body></html>"}' -H "Content-Type: application/json" REPLACE-WITH-YOUR-ENDPOINT


check in the S3 bucket

empty the s3 bucket before deleting

sls remove

