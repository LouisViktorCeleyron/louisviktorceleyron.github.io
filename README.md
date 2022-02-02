# louisviktorceleyron.github.io
De nos jours la vie est dur quand on est une petite patate
```cs 
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEditor;

[CustomPropertyDrawer(typeof(Aurevoir<>))]
public class PropertyDrawerDictionary : BasePropertyDrawer 
{
    internal override void OnGUIEffect(Rect position, SerializedProperty property)
    {
        Rect textRect = MakeRectForDrawer(0.1f,0f);
        Rect intRect= MakeRectForDrawer(0.9f, 0f);
        SerializedProperty bananeProp = property.FindPropertyRelative("banane");

        EditorGUI.LabelField(textRect, "Bite");
        EditorGUI.PropertyField(intRect, bananeProp, new GUIContent(""));
    }
}
```