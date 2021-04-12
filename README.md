# hello-world
first repository

Here is some new stuff to add to the new brach

module.exports = async ({ logger, configVars }, params) => {

incomingWebhookData = params.integrationTrigger.results.body.data;

  //process webhook data here and get the field operation id
  switch(incomingWebhookData.kind)
  {
    case "AgSync.Drive.Core.FieldOperationEvent+Created":
      fieldOperationId = incomingWebhookData.fieldOperation.id;
      break;
    case "AgSync.Drive.Core.FieldOperationEvent+Released":
      fieldOperationId = incomingWebhookData.id;
      break;
    case "AgSync.Drive.Core.FieldOperationEvent+AssignmentAdded":
      fieldOperationId = incomingWebhookData.id;
      break; 
    case "AgSync.Drive.Core.FieldOperationEvent+Verified":
      fieldOperationId = incomingWebhookData.id;
      break;   
  }
  
  apiEndpoint = `${configVars.baseUrl_PROD}/api/partners/integrations/${fieldOperationId}`;
  
  return { data: apiEndpoint}; 
}; 
