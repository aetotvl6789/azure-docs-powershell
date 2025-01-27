---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
---

# Get-AzCdnOrigin

## SYNOPSIS
Gets a CDN origin server.

> [!NOTE]
>This is the previous version of our documentation. Please consult [the most recent version](/powershell/module/az.cdn/get-azcdnorigin) for up-to-date information.

## SYNTAX

### ByFieldsParameterSet (Default)
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceIdParameterSet
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByObjectParameterSet
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.

## EXAMPLES

### Example 1
```powershell
Get-AzCdnOrigin -ResourceGroupName myresourcegroup -ProfileName mycdnprofile -EndpointName myendpoint
```

```Output
HostName                   : mystorage.blob.core.windows.net
HttpPort                   :
HttpsPort                  :
OriginHostHeader           :
Priority                   :
PrivateLinkApprovalMessage :
PrivateLinkLocation        :
PrivateLinkResourceId      :
Weight                     :
ResourceState              : Active
ResourceGroupName          : myresourcegroup
ProfileName                : mycdnprofile
EndpointName               : myendpoint
Id                         : /subscriptions/0b1f6471-1bf0-4dda-aec3-cb9272f09590/resourcegroups/myresourcegroup/providers/Micr
                             osoft.Cdn/profiles/mycdnprofile/endpoints/myendpoint/origins/mystorage
Name                       : mystorage
Type                       : Microsoft.Cdn/profiles/endpoints/origins
ProvisioningState          : Succeeded
```

## PARAMETERS

### -CdnEndpoint
Specifies the CDN endpoint object to which the origin belongs.

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointName
Specifies the name of the endpoint to which the origin server belongs.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OriginName
Specifies the name of the origin server.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProfileName
Specifies the name of the profile to which the origin server belongs.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of the resource group to which the origin server belongs.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
The resource id of the Azure CDN origin.

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint

## OUTPUTS

### Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin

## NOTES

## RELATED LINKS

[Set-AzCdnOrigin](./Set-AzCdnOrigin.md)


