# SSO

    => The term ToolBox we use here after is technically known as an Identity provider 
    => and Flora service is technically known as the resource server
    => the person that  wants to use Flora service and wants to login via ToolBox is technically called a client
    => Auth provider URL is the address to which the flora service redirects the user to complete the authentication 

## =========================================

    So the premise is that the person wants to use Flora service and doesn't want to go through the standard signup procedure of the service and would rather sign up or login via the ToolBox SSO being used by the service

    Broadly speaking from  the view of the person trying to access flora service the following events happen
    the client clicks on the sign in with ToolBox button on the service portal and is redirected to the Toolbox login website page where he is presented with a login form

    The person enters his details and is asked to give flora service the following permissions (whatever they may be)

    And then the person is redirected to flora service portal and is granted access to the service

## //=========================================

    From flora service point  of view when the person clicks on the login with Tool box button. 
    => A redirect request  attached with its App ID and App Secret registered with toolbox is made to the Auth provider URL
    => here the person is logged in to his toolBox account and asked to provide the permissions to the flora service 
    => then toolbox redirects the user to the Redirect URL registered by the Flora service attached with a code 
    => then Flora service receives the code sent by ToolBox 
    => Now Flora will send this code to the Auth Token URL of the toolBox which will return a access token to Flora
