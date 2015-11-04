# IIS Puppet Module

#### Table of Contents

1. [Overview](#overview)
2. [Module Description - What the module does and why it is useful](#module-description)
3. [Setup - The basics of getting started with codedeploy](#setup)
    * [What IIS affects](#what-IIS-affects)
4. [Usage - Configuration options and additional functionality](#usage)
5. [Limitations - OS compatibility, etc.](#limitations)

## Overview

This module installs and enables the IIS on Windows Servers.

## Module Description

The IIS module allows you to automatically host websites and applications in an AWS instance. 

## Setup

### What IIS Services affects,  add/remove files

* Packages
    * IIS Services (Windows)
    * DISM
    	Features Enabled
    	
    	 dism { "IIS-WebServerRole":            } ->
  		dism { "IIS-WebServer":                } ->
  		dism { "IIS-CommonHttpFeatures":       } ->
  		dism { "IIS-RequestFiltering":         } ->
  		dism { "IIS-StaticContent":            } ->
  		dism { "IIS-DefaultDocument":          } ->
  		dism { "IIS-DirectoryBrowsing":        } ->
  		dism { "IIS-HttpErrors":               } ->
  		dism { "IIS-ApplicationDevelopment":   } ->
  		dism { "IIS-ISAPIExtensions":          } ->
  		dism { "IIS-ISAPIFilter":              } ->
  		dism { "IIS-HealthAndDiagnostics":     } ->
  		dism { "IIS-HttpLogging":              } ->
  		dism { "IIS-Security":                 } ->
  		dism { "IIS-BasicAuthentication":      } ->
  		dism { "IIS-WindowsAuthentication":    } ->
  		dism { "IIS-Performance":              } ->
  		dism { "IIS-HttpCompressionStatic":    } ->
  		dism { "IIS-WebServerManagementTools": } ->
  		dism { "IIS-ManagementConsole":        } ->
  		dism { "IIS-ManagementScriptingTools":  } 
    
* Services
    * IIS Webserver

## Usage

Install IIS in Windows Server and ensure the Service is running

    class {'iis': }

## Limitations

* Windows 2012 Server
* Windows 2008 Server

