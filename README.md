# helo ![wavey](https://raw.githubusercontent.com/FragileDeviations/FragileDeviations/main/wavey.gif)

i mainly do stuff with unity

> [!CAUTION]
> very dumb

## cool stuff
> ### [UnitySceneAutoSave](https://github.com/WeatherElectric/UnitySceneAutoSave)
> 
> Automatically save the currently open scene in Unity Editor.

> ### [VoidSpeaker](https://github.com/WeatherElectric/VoidSpeaker)
>
> A BONELAB media player.

> ### [RecursiveSelfImprovement](https://github.com/WeatherElectric/RecursiveSelfImprovement)
>
> A general quality of life/tools mod for BONELAB.

## other cool stuff
> ### [this guy](https://www.nin.com/)
> ![reznor](https://raw.githubusercontent.com/FragileDeviations/FragileDeviations/main/reznor.png)



## look at these great method names
```cs
[ServerRpc(RequireOwnership = false)]
public void ChallengerExplosionServerRpc()
{
    _willExplode.Value = true;
    ChallengerExplosionClientRpc();
}

[ClientRpc]
public void ChallengerExplosionClientRpc()
{
   StartCoroutine(ChallengerExplosion());
   _exploding = true;
}


private IEnumerator ChallengerExplosion()
{
   yield return new WaitForSeconds(1f);

   _audioSource.PlayOneShot(explodeNoise, 1);
   Utilities.PlayAudibleNoise(_audioSource, explodeNoise, transform.position, 17f, 1, isInElevator);

   yield return new WaitForSeconds(timeBeforeExplosion);

   Utilities.CreateExplosion(transform.position, true, 100, 0f, 6.4f);

   yield return new WaitForSeconds(2f);

   if (IsServer) gameObject.GetComponent<NetworkObject>().Despawn();
}
```
