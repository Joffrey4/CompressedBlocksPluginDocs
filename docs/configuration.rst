Configuration
=============

|   Currently, the configuration file handle the lores and the blocks textures. It is generated automatically when you start your server, after having put the **plugin.jar** into your "plugins" directory.
|
|   This file may change in the next updates: new configuration nodes could be added or removed. To get the last version of the file, simply delete the current one. Another file will be generated by the plugin. Or, for any reason, if you don't want to delete your configuration file, you can refer to the `Up-to-date config file <https://github.com/Joffrey4/CompressedBlocksPlugin/blob/master/Plugin/src/main/resources/config.yml>`_ to copy your missing nodes.

Common lore
-----------

.. warning:: Do not edit any lore if you have already setup a server, and compressed some blocks. A lore modification is applied only to the newly compressed blocks. And they won't be stackable with the blocks that still have the old lore.

You can personalize the lores of the compressed blocks. When **lore.usecommon** is set to true, all blocks get the **lore.common** below. You can naturally edit this lore, like this::

    lore:
      usecommon: true
      common:
        - "I'm packing and amount"
        - "of 9 &type !"
        - "Isn't that cool ?"

The **&type** is automatically replaced by the type of the block. Ex: Compressed Stone type is ‘Stone’.

Detailed lores
--------------

You can event set a specific lore for each blocks, with the size that you want and with as many lines as you want. For this, you need first to false **lore.usecommon**. And then, you can uncomment the desired blocks and fill in the lore. Like this::

    lore:
      usecommon: false

      detailed:
        oakwood:
          - 'Another lore specific'
          - 'to the &type !'
        gravel:
          - "Enjoy me, I'm a"
          - 'Compressed &type !'

The blocks that aren’t filled in the **lore.detailed** will automatically use the **lore.common**.

Textures
--------

.. warning:: Do not edit the textures if you have already setup a server, and compressed some blocks. Changing the texture will result in the lose of all compressed blocks previously made.

You can personalize the textures of the compressed blocks by following `this tutorial <https://bukkit.org/threads/create-your-own-custom-head-texture.424286/>`_. It will teach you how to create and upload your texture file to `http://minecraft.net <http://minecraft.net>`_. Because in the configuration file, the code next to each block is a part of the link of a picture uploaded to `http://minecraft.net <http://minecraft.net>`_.

Once you have followed the tutorial, you got a link similar to this::

    http://textures.minecraft.net/texture/b79bd6534a7d9def47aa7ccc52b330f454520eb18dbaf

Simply copy the code of the picture into the configuration file.