---
external help file: 
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustoattacheddatabaseconfigurationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/Kusto/help/Test-AzKustoAttachedDatabaseConfigurationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/Kusto/help/Test-AzKustoAttachedDatabaseConfigurationNameAvailability.md
---

# Test-AzKustoAttachedDatabaseConfigurationNameAvailability

## SYNOPSIS
Checks that the attached database configuration resource name is valid and is not already in use.

## SYNTAX

### CheckExpanded (Default)
```
Test-AzKustoAttachedDatabaseConfigurationNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### CheckViaIdentityExpanded
```
Test-AzKustoAttachedDatabaseConfigurationNameAvailability -InputObject <IKustoIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Checks that the attached database configuration resource name is valid and is not already in use.

## EXAMPLES

### Example 1: Checks whether the attached database configuration name is available in the given cluster
```powershell
Test-AzKustoAttachedDatabaseConfigurationNameAvailability -ResourceGroupName "testrg" -ClusterName "mycluster" -Name "testdatabase"
```

```output
Message Name               NameAvailable Reason
------- ----               ------------- ------
        testdatabase       True
```

The above command returns whether or not an attached database configuration name is available in the cluster named "mycluster" in resource group "testrg".

## PARAMETERS

### -ClusterName
The name of the Kusto cluster.

```yaml
Type: System.String
Parameter Sets: CheckExpanded
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
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter
To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Attached database resource name.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
The name of the resource group containing the Kusto cluster.

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Gets subscription credentials which uniquely identify Microsoft Azure subscription.
The subscription ID forms part of the URI for every service call.

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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

### Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20220201.ICheckNameResult

## NOTES

ALIASES

COMPLEX PARAMETER PROPERTIES

To create the parameters described below, construct a hash table containing the appropriate properties. For information on hash tables, run Get-Help about_Hash_Tables.


INPUTOBJECT <IKustoIdentity>: Identity Parameter
  - `[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.
  - `[ClusterName <String>]`: The name of the Kusto cluster.
  - `[DataConnectionName <String>]`: The name of the data connection.
  - `[DatabaseName <String>]`: The name of the database in the Kusto cluster.
  - `[Id <String>]`: Resource identity path
  - `[Location <String>]`: Azure location (region) name.
  - `[ManagedPrivateEndpointName <String>]`: The name of the managed private endpoint.
  - `[OperationId <String>]`: The Guid of the operation ID
  - `[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.
  - `[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection.
  - `[PrivateLinkResourceName <String>]`: The name of the private link resource.
  - `[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.
  - `[ScriptName <String>]`: The name of the Kusto database script.
  - `[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

## RELATED LINKS

