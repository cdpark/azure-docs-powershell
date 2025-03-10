---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: 
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/Security/Security/help/New-AzSecurityAutomation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/Security/Security/help/New-AzSecurityAutomation.md
---

# New-AzSecurityAutomation

## SYNOPSIS
Creates new security automation

## SYNTAX

### ResourceGroupLevelResource (Default)
```
New-AzSecurityAutomation -ResourceGroupName <String> -Name <String> -Location <String> [-Etag <String>]
 [-Tag <Hashtable>] [-Description <String>] [-IsEnabled <Boolean>] -Scope <PSSecurityAutomationScope[]>
 -Source <PSSecurityAutomationSource[]> -Action <PSSecurityAutomationAction[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
New-AzSecurityAutomation -ResourceId <String> -Location <String> [-Etag <String>] [-Tag <Hashtable>]
 [-Description <String>] [-IsEnabled <Boolean>] -Scope <PSSecurityAutomationScope[]>
 -Source <PSSecurityAutomationSource[]> -Action <PSSecurityAutomationAction[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
New-AzSecurityAutomation [-Location <String>] [-Etag <String>] [-Tag <Hashtable>] [-Description <String>]
 [-IsEnabled <Boolean>] [-Scope <PSSecurityAutomationScope[]>] [-Source <PSSecurityAutomationSource[]>]
 -Action <PSSecurityAutomationAction[]> -InputObject <PSSecurityAutomation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Creates new security automation

## EXAMPLES

### Example 1
```powershell
PS C:\> New-AzSecurityAutomation -Name 'ampleAutomation' -ResourceGroupName 'SampleResourceGroup' -Description 'Sample security automation' -Scope $scopes -Source $sources -Action $actions
```

Creates new security automation named "SampleAutomation" under resource group named "SampleResourceGroup"

## PARAMETERS

### -Action
A collection of the actions which are triggered if all the configured rules evaluations, within at least one rule set, are true

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Automations.PSSecurityAutomationAction[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

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

### -Description
The security automation description

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

### -Etag
Entity tag is used for comparing two or more entities from the same requested resource

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

### -InputObject
Input Object.

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Automations.PSSecurityAutomation
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsEnabled
Is rule enabled.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Location.

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Resource name.

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Resource group name.

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID of the security resource that you want to invoke the command on.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Scope
A collection of scopes on which the security automations logic is applied.
Supported scopes are the subscription itself or a resource group under that subscription.
The automation will only apply on defined scopes

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Automations.PSSecurityAutomationScope[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Automations.PSSecurityAutomationScope[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Source
A collection of the source event types which evaluate the security automation set of rules

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Automations.PSSecurityAutomationSource[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Automations.PSSecurityAutomationSource[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Tags.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

### Microsoft.Azure.Commands.Security.Models.Automations.PSSecurityAutomation

## OUTPUTS

### Microsoft.Azure.Commands.Security.Models.Automations.PSSecurityAutomation

## NOTES

## RELATED LINKS
