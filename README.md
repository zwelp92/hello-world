# hello-world
first repository

branch-#2
Creating a second branch but not creating a pull request
=======
This is a new branch to compare changes being made to the others.
main
Here is some new stuff to add to the new brach

module.exports = async ({ logger, configVars }, params) => {

incomingWebhookData = params.integrationTrigger.results.body.data;

  //process webhook data here and get the field operation id
  
  apiEndpoint = `${configVars.baseUrl_PROD}/api/partners/integrations/${fieldOperationId}`;
  
  return { data: apiEndpoint}; 
}; 
