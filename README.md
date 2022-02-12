# Chest
//This code is from Epitome's tutorial https://www.youtube.com/watch?v=b8YUfee_pzc&t=23003s
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Chest : Collectable
{
	public Sprite emptyChest;
	public int pesosAmount = 5;

	protected override void OnCollect()
	{
		if (!collected) {
			collected = true;
			GetComponent<SpriteRenderer> ().sprite = emptyChest;
			GameManager.instance.pesos += pesosAmount;
			GameManager.instance.ShowText ("+" + pesosAmount + "Gold!", 25, Color.yellow, transform.position, Vector3.up * 50, 3.0f); 
				

		}

	}

}
