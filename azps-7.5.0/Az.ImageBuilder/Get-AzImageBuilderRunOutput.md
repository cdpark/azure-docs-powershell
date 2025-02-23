---
external help file: 
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
---

# Get-AzImageBuilderRunOutput

## SYNOPSIS
Get the specified run output for the specified image template resource

> [!NOTE]
>This is the previous version of our documentation. Please consult [the most recent version](/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput) for up-to-date information.

## SYNTAX

### List (Default)
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Get
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## DESCRIPTION
Get the specified run output for the specified image template resource

## EXAMPLES

### Example 1: List all run results under a template
```powershell
Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder
```

```output
Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

This command lists all run results under a template.

### Example 2: Get a run result under a template
```powershell
Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 
```

```output
Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

This command gets a run result under a template.

### Example 3: Get a run result under a template
```powershell
$result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
Get-AzImageBuilderRunOutput -InputObject $result
```

```output
Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

This command gets a run result under a template.

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageTemplateName
The name of the image Template

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter
To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
The name of the resource group.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunOutputName
The name of the run output

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Subscription credentials which uniquely identify Microsoft Azure subscription.
The subscription Id forms part of the URI for every service call.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput

## NOTES

ALIASES

COMPLEX PARAMETER PROPERTIES

To create the parameters described below, construct a hash table containing the appropriate properties. For information on hash tables, run Get-Help about_Hash_Tables.


INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter
  - `[Id <String>]`: Resource identity path
  - `[ImageTemplateName <String>]`: The name of the image Template
  - `[ResourceGroupName <String>]`: The name of the resource group.
  - `[RunOutputName <String>]`: The name of the run output
  - `[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription Id forms part of the URI for every service call.

## RELATED LINKS

