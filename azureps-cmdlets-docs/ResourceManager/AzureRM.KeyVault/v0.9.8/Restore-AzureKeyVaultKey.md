---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 9781A7D4-50B7-493A-9D4A-90ED291BD15A
---

# Restore-AzureKeyVaultKey

## SYNOPSIS
Creates a key in a vault from a backed-up key.

## SYNTAX

```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-Profile <AzureProfile>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.
This key is a replica of the backed-up key in the input file and has the same name as the original key.
If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.
If the backup contains multiple versions of a key, all versions are restored.

The key vault that you restore the key into can be different from the key vault that you backed up the key from.
However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).
See the Microsoft Azure Trust Centerhttps://azure.microsoft.com/support/trust-center/ (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.

## EXAMPLES

### Example 1: Restore a backed-up key
```
PS C:\>Restore-AzureKeyVaultKey -VaultName "MyKeyVault" -InputFile "C:\Backup.blob"
```

This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.

## PARAMETERS

### -InputFile
Specifies the input file that contains the backup of the key to restore.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Specifies the Azure profile from which this cmdlet reads.
If you do not specify a profile, this cmdlet reads from the local default profile.

```yaml
Type: AzureProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Specifies the name of the key vault into which to restore the key.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Backup-AzureKeyVaultKey](./Backup-AzureKeyVaultKey.md)

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)


