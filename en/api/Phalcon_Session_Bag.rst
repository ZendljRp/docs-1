Class **Phalcon\\Session\\Bag**
===============================

*implements* :doc:`Phalcon\\DI\\InjectionAwareInterface <Phalcon_DI_InjectionAwareInterface>`, :doc:`Phalcon\\Session\\BagInterface <Phalcon_Session_BagInterface>`, IteratorAggregate, Traversable, ArrayAccess, Countable

This component helps to separate session data into "namespaces". Working by this way you can easily create groups of session variables into the application  

.. code-block:: php

    <?php

    $user = new \Phalcon\Session\Bag('user');
    $user->name = "Kimbra Johnson";
    $user->age = 22;



Methods
-------

public  **__construct** (*string* $name)

Phalcon\\Session\\Bag constructor



public  **setDI** (:doc:`Phalcon\\DiInterface <Phalcon_DiInterface>` $dependencyInjector)

Sets the DependencyInjector container



public :doc:`Phalcon\\DiInterface <Phalcon_DiInterface>`  **getDI** ()

Returns the DependencyInjector container



public  **initialize** ()

Initializes the session bag. This method must not be called directly, the class calls it when its internal data is accesed



public  **destroy** ()

Destroys the session bag 

.. code-block:: php

    <?php

     $user->destroy();




public  **set** (*string* $property, *string* $value)

Sets a value in the session bag 

.. code-block:: php

    <?php

     $user->set('name', 'Kimbra');




public *mixed*  **get** (*string* $property, [*string* $defaultValue])

Obtains a value from the session bag optionally setting a default value 

.. code-block:: php

    <?php

     echo $user->get('name', 'Kimbra');




public *boolean*  **has** (*string* $property)

Check whether a property is defined in the internal bag 

.. code-block:: php

    <?php

     var_dump($user->has('name'));




public *boolean*  **remove** (*string* $property)

Removes a property from the internal bag 

.. code-block:: php

    <?php

     $user->remove('name');




public  **getIterator** ()

...


public *string*  **__get** (*string* $property)

Magic getter to obtain values from the session bag. 

.. code-block:: php

    <?php

     echo $user->name;




public  **__set** (*string* $property, *string* $value)

Magic setter to assign values to the session bag. Alias for Phalcon\\Session\\Bag::set() 

.. code-block:: php

    <?php

     $user->name = "Kimbra";




public *boolean*  **__isset** (*string* $property)

Magic isset to check whether a property is defined in the bag. Alias for Phalcon\\Session\\Bag::has() 

.. code-block:: php

    <?php

     var_dump(isset($user['name']));




public *boolean*  **__unset** (*string* $property)

Magic unset to remove items using the property syntax. Alias for Phalcon\\Session\\Bag::remove() 

.. code-block:: php

    <?php

     unset($user['name']);




public  **offsetGet** (*unknown* $property)

...


public  **offsetSet** (*unknown* $property, *unknown* $value)

...


public  **offsetExists** (*unknown* $property)

...


public  **offsetUnset** (*unknown* $property)

...


public  **count** ()

...


