---
title: Displaying verification statuses for all of your commits
shortTitle: Displaying verification for all commits
intro: You can enable vigilant mode for commit signature verification to mark all of your commits and tags with a signature verification status.
versions:
  fpt: '*'
  ghec: '*'
topics:
  - Identity
  - Access management
redirect_from:
  - /github/authenticating-to-github/displaying-verification-statuses-for-all-of-your-commits
  - /github/authenticating-to-github/managing-commit-signature-verification/displaying-verification-statuses-for-all-of-your-commits
---
{% data reusables.identity-and-permissions.vigilant-mode-beta-note %}

## About vigilant mode

When you work locally on your computer, Git allows you to set the author of your changes and the identity of the committer. This, potentially, makes it difficult for other people to be confident that commits and tags you create were actually created by you. To help solve this problem you can sign your commits and tags. For more information, see "[Signing commits](/github/authenticating-to-github/signing-commits)" and "[Signing tags](/github/authenticating-to-github/signing-tags)." {% data variables.product.prodname_dotcom %} marks signed commits and tags with a verification status. 

De forma predeterminada, las confirmaciones y las etiquetas se marcan como "Verificadas" si se firman con una clave GPG o S/MIME que se verificó correctamente. Si una confirmación o etiqueta tiene una firma que {% data variables.product.prodname_dotcom %} no puede verificar, marcamos la confirmación o la etiqueta como "No verificada". En todos los demás casos, no se muestra el estado de verificación.
lo 
Sin embargo, puede brindarles a otros usuarios una mayor confianza en la identidad atribuida a sus confirmaciones y etiquetas al habilitar el modo vigilante en su configuración de {% data variables.product.prodname_dotcom %}. Con el modo vigilante habilitado, todas sus confirmaciones y etiquetas se marcan con uno de los tres estados de verificación
youltimo

![Signature verification statuses](/assets/images/help/commits/signature-verification-statuses.png)

{% data reusables.identity-and-permissions.vigilant-mode-verification-statuses %}

You should only enable vigilant mode if you sign all of your commits and tags and use an email address that is verified for your account on {% data variables.product.product_name %} as your committer email address. After enabling this mode, any unsigned commits or tags that you generate locally and push to {% data variables.product.prodname_dotcom %} will be marked "Unverified."

{% data reusables.identity-and-permissions.verification-status-check %}

## Enabling vigilant mode

{% data reusables.user-settings.access_settings %}
{% data reusables.user-settings.ssh %}
3. On the SSH Settings page, under "Vigilant mode," select **Flag unsigned commits as unverified**.

   ![Flag unsigned commits as unverified checkbox](/assets/images/help/commits/vigilant-mode-checkbox.png)
