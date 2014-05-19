Minecraft-Plugin-Entity-Interaction
===================================

package me.MustardMan227.EntityInteraction;

import java.util.logging.Logger;

public class EntityInteraction extends JavaPlugin {
	public static Bukkit plugin; 
	public final Logger logger = Logger.getLogger("Minecraft");
	public final BukkitListener ml = new BukkitListener(this);
	public final BukkitLogger blo = new BukkitLogger(this);
	
	public void onEnable() {
		blo.enabled(true);
		PluginManager pm = this.getServer().getPluginManager();
		pm.registerEvents(ml, this);
	}
	
	public void onDisable() {
		blo.enabled(false);
	}
	
	public boolean onCommand(CommandSender sender, Command cmd,
			String commandLable, String[] args) {
		return false;
	}

}
