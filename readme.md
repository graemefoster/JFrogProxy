#JFrog Proxy

A repository to help Azure App Service consume JFrog repositories over a virtual network.

## TLDR;

> You don't need this unless you are pulling over a virtual network

Azure App Service issues docker commands that JFrog doesn't handle very well, and returns old manifest files 
that App Service cannot handle.

This application is a simple YARP proxy to remove a querystring that causes JFrog to return old manifests.

## Configuration

Set an app setting ``` ReverseProxy__Clusters__containerRegistryCluster__Destinations__destination1__Address ``` to the host name of your JFrog instance.

Reference an image via the proxy hostname.


